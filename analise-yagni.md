# Item 3 da atividade

YAGNI (*You Aren't Gonna Need It*) recomenda implementar uma capacidade quando há uma necessidade atual, e não apenas porque ela talvez seja útil. A versão original precisava somente cadastrar, autenticar e listar usuários.

## Item 3.a: análise do princípio YAGNI

### Atributos desnecessários de `Usuario`

| Atributo | Motivo da violação |
|---|---|
| `id` | Nenhum requisito pede identificação ou busca por identificador. |
| `data_cadastro` | Não há consulta, auditoria ou relatório por data. |
| `ultimo_login` | Autenticar não exige registrar a última autenticação. |
| `perfil` | Não existem tipos de usuário no escopo atual. |
| `permissoes` | Não há autorização baseada em permissões. |
| `configuracoes` | Preferências personalizadas não foram solicitadas. |
| `historico_logins` | O requisito pede validação, não auditoria de acessos. |
| `foto_perfil_url` | Foto de perfil está fora do cadastro mínimo. |
| `telefone` | O cadastro exige apenas nome, e-mail e senha. |
| `endereco` | Não participa de nenhuma função necessária. |
| `empresa` | Dados profissionais não foram pedidos. |
| `cargo` | Dados profissionais não foram pedidos. |
| `departamento` | Dados profissionais não foram pedidos. |

`nome`, `email` e `senha` são necessários. A senha permanece como hash por ser uma proteção básica, não uma funcionalidade futura.

Além disso, `GerenciadorUsuarios` tinha `cache` e `indice_email`. Ambos duplicavam o estado de `usuarios` e exigiam sincronização. Para a escala não especificada da atividade, percorrer a lista é suficiente e mais simples.

### Métodos desnecessários

#### Em `Usuario`

| Método | Motivo da violação |
|---|---|
| `_gerar_id` | Só sustenta o atributo `id`, que não é necessário. |
| `adicionar_permissao` | Antecipa um sistema de autorização inexistente. |
| `remover_permissao` | Antecipa manutenção de permissões. |
| `tem_permissao` | Antecipa consultas de autorização. |
| `atualizar_configuracao` | Não há requisito de preferências. |
| `registrar_login` | Cria auditoria e histórico não solicitados. |
| `exportar_json` | Não foi solicitada exportação. |
| `exportar_xml` | Adiciona um segundo formato de exportação sem consumidor atual. |
| `atualizar_foto_perfil` | Não há foto de perfil no escopo. |
| `atualizar_dados_profissionais` | Não há dados profissionais no escopo. |

O construtor, `_hash_senha` e `validar_senha` permanecem porque criam o usuário com segurança básica e suportam diretamente o login.

#### Em `GerenciadorUsuarios`

| Método | Motivo da violação |
|---|---|
| `_atualizar_cache` | Mantém uma estrutura redundante usada apenas por função futura. |
| `buscar_por_id` | Busca por ID não foi pedida. |
| `buscar_por_perfil` | Perfis não fazem parte dos requisitos. |
| `buscar_por_permissao` | Permissões não fazem parte dos requisitos. |
| `exportar_todos_json` | Exportação não foi solicitada. |
| `importar_usuarios_json` | Importação não foi solicitada e o método sequer tinha implementação. |
| `gerar_relatorio_atividade` | Relatórios e métricas de atividade estão fora do escopo. |

`cadastrar`, `fazer_login` e `listar_todos` permanecem por corresponderem exatamente aos três casos de uso atuais. Remover os demais itens reduz dependências, estados duplicados e caminhos que precisariam ser testados e mantidos.

## Item 3.b: simplificação do código

O arquivo `src/usuario_simples.py` foi reduzido aos dados `nome`, `email` e `senha` e às operações de cadastro, login e listagem. O hash da senha e a validação de email duplicado foram mantidos por serem requisitos essenciais da atividade.

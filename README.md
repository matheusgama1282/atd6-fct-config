# atd6-fct-config

Configuração canônica (critérios de teste) do **SW FCT ATD6**.

> ⚠️ **Não editar à mão.** Este repositório é a fonte única dos critérios de teste e é
> atualizado **automaticamente pelo software FCT** (publicação assinada pela engenharia da
> Autotrac). Edições manuais quebram a assinatura e serão **rejeitadas** pelo software.

## Arquivos

- **`parametros.json`** — critérios de teste não-secretos (limites, regras de identificação,
  tolerâncias, versões esperadas). Campos `config_version` (inteiro monotônico) e
  `config_updated_at` (UTC) controlam a versão.
- **`parametros.sig`** — assinatura RSA-PSS-SHA256 (base64) dos bytes exatos de
  `parametros.json`. O software verifica com a chave pública embarcada antes de adotar a
  configuração.

## O que NÃO está aqui

Segredos (string de conexão, credenciais) e amarrações de máquina (portas COM, paths de log,
calibração por bancada) ficam **locais** em cada instalação — nunca neste repositório.

Ver `DOCS/PRD_config_remota_github.md` no repositório do software.

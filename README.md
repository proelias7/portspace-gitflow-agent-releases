# PortSpace Gitflow Agent — Releases

Repositório público de **binários e instalador** do agent Windows do [PortSpace Gitflow](https://gitflow.portspace.com.br).

> O código-fonte do agent fica no repositório privado `portspacev2`. Este repo contém apenas artefatos assinados para instalação.

## Instalação rápida

1. No painel Gitflow, crie um ambiente e clique em **Gerar conexão** (código `gfe_...`, válido por 30 minutos).
2. Baixe o instalador ou use o comando copiado no painel.
3. Execute no PowerShell **como Administrador**:

```powershell
irm https://github.com/proelias7/portspace-gitflow-agent-releases/releases/latest/download/install-service.ps1 -OutFile install-service.ps1
.\install-service.ps1 `
  -ServiceUrl "wss://gitflow.portspace.com.br/v1/agent" `
  -EnrollmentCode "gfe_SEU_CODIGO" `
  -ReleasePublicKey "HoCh+IszDl+Lyj4iU0QChxymX79qa4v2Z7hPK/H16FY="
```

## Assets da release

| Arquivo | Descrição |
|---------|-----------|
| `install-service.ps1` | Instalador do serviço Windows |
| `gitflow-agent-windows-amd64.exe` | Binário principal do agent |
| `gitflow-agent-updater-windows-amd64.exe` | Atualizador automático |
| `gitflow-agent-importer-windows-amd64.exe` | Importador de repositórios |
| `gitflow-agent-tray.ps1` | Script da bandeja do sistema |
| `manifest-windows-amd64.json` | Manifesto assinado Ed25519 |

## Verificação de assinatura

Os binários são publicados com manifesto assinado. A chave pública acima (`ReleasePublicKey`) é usada pelo instalador para validar os artefatos antes de instalar.

## Links

- [Última release](https://github.com/proelias7/portspace-gitflow-agent-releases/releases/latest)
- [Painel Gitflow](https://portspace.com.br) (requer login PortSpace)

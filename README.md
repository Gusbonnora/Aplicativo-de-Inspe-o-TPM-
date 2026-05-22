# ⚙️ Checklist de Manutenção Autônoma — BEL

Aplicativo web para registro de inspeções de manutenção autônoma em equipamentos industriais, otimizado para uso em **tablets via navegador**, sem necessidade de instalação.

---

## 📋 Sobre o projeto

Este aplicativo foi desenvolvido para digitalizar e padronizar o processo de inspeção de equipamentos no chão de fábrica. O colaborador acessa pelo navegador do tablet, preenche o checklist, tira fotos de comprovação ao vivo e assina digitalmente ao concluir. Todos os registros ficam salvos com data e hora para rastreabilidade completa.

---

## ✅ Funcionalidades

### Para o colaborador
- Identificação com **matrícula e nome completo** (mínimo dois nomes obrigatórios)
- Seleção do equipamento antes de iniciar
- Checklist com até **10 itens configuráveis**
- Visualização da **foto de referência** (padrão aceitável) de cada item
- Status por item: **Conforme**, **Atenção** ou **Não conforme**
- **Captura de foto obrigatória** por item via câmera ao vivo — galeria bloqueada
- Campo de observações por item
- **Assinatura digital** ao finalizar
- Botão de **cancelar inspeção** com confirmação
- Alerta em tempo real para itens não conformes

### Para o administrador
- Acesso protegido por **senha** (padrão: `admin123`)
- Ativar ou desativar cada item do checklist
- Personalizar **título e descrição** de cada item
- Fazer upload da **foto de referência** de cada item
- Fazer upload da **logo da empresa**

### Histórico e relatórios
- Todos os registros salvos **permanentemente** no dispositivo
- Filtro por: Todos / Conformes / Com não conformidade
- Detalhe completo de cada inspeção: fotos, status, observações, assinatura
- Registro de **data e hora de início, conclusão e de cada foto**
- Exportação em **PDF** via impressão do navegador

---

## 🚀 Como publicar (sem precisar programar)

### Passo 1 — Baixe o arquivo
No painel do chat, clique nos três pontinhos do arquivo e selecione **Download**. O arquivo se chama `checklist_manutencao.html`.

### Passo 2 — Publique gratuitamente no Netlify
1. Acesse [netlify.com](https://netlify.com) e crie uma conta gratuita
2. Na tela inicial, localize a área **"Deploy manually"** ou **"Drop your files here"**
3. Arraste o arquivo `checklist_manutencao.html` para essa área
4. Aguarde alguns segundos — você receberá um link, por exemplo:
   ```
   https://minha-empresa-checklist.netlify.app
   ```

### Passo 3 — Acesse no tablet
1. Abra o **Google Chrome** no tablet
2. Digite o link gerado pelo Netlify
3. Toque no menu do navegador → **"Adicionar à tela inicial"** para criar um atalho de acesso rápido

> ⚠️ **Importante:** Para que a câmera funcione corretamente, o site precisa ser acessado via **HTTPS**. O Netlify já fornece HTTPS gratuitamente. Não abra o arquivo diretamente do computador (arquivo local), pois a câmera será bloqueada pelo navegador.

---

## 🔧 Configuração inicial (administrador)

Após publicar, acesse o aplicativo e siga os passos:

1. Na tela inicial, toque em **"⚙️ Administrador"**
2. Digite a senha padrão: `admin123`
3. Configure os itens do checklist:
   - Ative ou desative cada item com o botão de toggle
   - Edite o título e a descrição de cada item
   - Faça upload da foto de referência (padrão aceitável) de cada item
4. Na seção **"Logo da empresa"**, faça upload da logo oficial
5. Toque em **"💾 Salvar configuração"**

> 💡 Recomenda-se alterar a senha padrão diretamente no código antes de publicar. Localize `admin123` no arquivo `.html` e substitua pela senha desejada.

---

## 📱 Requisitos

| Item | Requisito |
|------|-----------|
| Dispositivo | Tablet ou computador com navegador moderno |
| Navegador | Google Chrome (recomendado) ou Safari |
| Conexão | Necessária apenas para carregar o app pela primeira vez |
| Câmera | Câmera traseira obrigatória para fotos de comprovação |
| Armazenamento | Os dados ficam salvos no próprio navegador do dispositivo (localStorage) |

---

## ⚠️ Limitações importantes

- Os dados são salvos **no navegador do tablet**. Se o cache/dados do navegador forem limpos, os registros serão perdidos.
- Para ambiente de produção com múltiplos dispositivos ou backup em nuvem, recomenda-se integrar um **banco de dados backend** (ex: Firebase, Supabase ou similar).
- O bloqueio de galeria depende do suporte do navegador ao `getUserMedia`. Funciona corretamente no Chrome e Safari em dispositivos móveis via HTTPS.

---

## 🗂️ Estrutura do arquivo

O aplicativo é um único arquivo `.html` autocontido que inclui:

```
checklist_manutencao.html
├── HTML — estrutura das telas
├── CSS  — estilos e layout responsivo
└── JS   — lógica, câmera, armazenamento e relatórios
```

Não há dependências externas, frameworks ou bibliotecas. Funciona offline após o primeiro carregamento.

---

## 📄 Licença

Desenvolvido sob demanda para uso interno da **BEL**. Todos os direitos reservados.

---

## 👤 Suporte

Em caso de dúvidas ou necessidade de ajustes, entre em contato com o responsável pelo desenvolvimento do aplicativo.

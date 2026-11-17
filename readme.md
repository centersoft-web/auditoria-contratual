════════════════════════════════════════════════════════════════════
   📜 AUDITORIA CONTRATUAL — SUITE DE ANÁLISE JURÍDICA
   🏛️  by Center Soft Inc.®
════════════════════════════════════════════════════════════════════


📌 1. DESCRIÇÃO GERAL
────────────────────────────────────────────────────────────────────

O arquivo index.html implementa a camada de entrada (launcher) de uma
suíte local de auditoria contratual. Ele não contém, por si só, as
regras de análise jurídica: essas regras ficam nos módulos carregados
dentro de um iframe.

A aplicação oferece autenticação por senha mestre, navegação lateral,
tela inicial com cartões dos módulos, backup completo dos dados do
navegador (LocalStorage e IndexedDB), restauração completa e reset
total.

Toda a operação é local. Não há servidor externo, banco de dados em
nuvem ou sincronização automática. As informações ficam armazenadas
na memória do navegador do usuário.


✨ 2. FUNCIONALIDADES PRINCIPAIS
────────────────────────────────────────────────────────────────────

🔐 Login com senha mestre armazenada no LocalStorage, na chave
   "senhaMaster".

🚪 Se a senha estiver vazia, o acesso é direto, sem bloqueio.

🔒 Sidebar bloqueada enquanto o usuário não estiver autenticado.

🏠 Tela inicial com cartões clicáveis para os módulos disponíveis.

🧭 Navegação entre módulos por meio da sidebar e dos cartões da
   tela inicial.

🖼️ Carregamento dos módulos em iframe, com controle do item ativo
   no menu.

↩️ Botão de retorno à tela inicial por meio do logo "A" na sidebar.

⚙️ Painel de Configurações com alteração de senha, backup completo,
   restauração completa, reset total e aviso de política de uso.

📥 Backup completo de todas as chaves do LocalStorage e de todos
   os bancos do IndexedDB.

📤 Restauração completa com relatório de bancos restaurados,
   registros gravados e falhas.

🛡️ Fechamento seguro do iframe antes de operações de backup,
   restauração ou reset.

🗂️ Nome padronizado do arquivo de backup:
   Backup_Auditoria_<AAAA>_<DD-MM-AAAA>_<HH>h<MM>.json


🧩 3. MÓDULOS DISPONÍVEIS
────────────────────────────────────────────────────────────────────

🏠 Auditor de Locação
   Arquivo esperado: Auditor de Locação.html
   Descrição: Analisa contratos de locação residencial contra a
   Lei do Inquilinato (Lei 8.245/91).
   Regras citadas na interface: 10 regras — Arts. 4º, 17, 22, 23,
   35, 37, 45 e 58.

🏡 Auditor de Compra e Venda
   Arquivo esperado: Auditor de Compra & Venda.html
   Descrição: Analisa contratos de compra e venda de imóvel ou
   veículo contra o Código Civil.
   Regras citadas na interface: 14 regras — Arts. 104, 125, 412,
   417, 441, 447, 481 e 500.

📎 Observação: os arquivos dos módulos não estão incluídos no
   index.html. Eles devem estar no mesmo diretório da aplicação,
   com os nomes exatos acima.


💻 4. REQUISITOS
────────────────────────────────────────────────────────────────────

🌐 Navegador moderno com suporte a LocalStorage, IndexedDB, Blob,
   URL.createObjectURL e FileReader.

📚 Recomenda-se um navegador que também ofereça indexedDB.databases()
   para exportação completa dos bancos.

🛰️ Conexão com a internet apenas para carregar as fontes do Google
   Fonts (Cinzel e Montserrat) e a imagem de fundo do Unsplash.

📴 Para uso offline, baixe as fontes e a imagem e ajuste o CSS.

🖥️ Não é necessário servidor backend. A aplicação pode ser servida
   por qualquer servidor estático.


⚙️ 5. INSTALAÇÃO
────────────────────────────────────────────────────────────────────

1️⃣ Baixe ou clone os arquivos do projeto.

2️⃣ Coloque o index.html na raiz do diretório.

3️⃣ Coloque os módulos no mesmo diretório:
      • Auditor de Locação.html
      • Auditor de Compra & Venda.html

4️⃣ Opcionalmente, adicione um arquivo icon.ico no mesmo diretório
   para o favicon.

5️⃣ Abra o index.html no navegador.

💡 Recomendação: servir a aplicação por HTTP, e não abrir diretamente
   via file://, pois alguns navegadores restringem IndexedDB e
   iframes nesse modo.

Exemplos de servidor local:

🐍 Com Python 3:
      python -m http.server 8000

🟩 Com Node.js:
      npx serve .

Depois, acesse http://localhost:8000 no navegador.


🖥️ 6. INSTALAÇÃO NO COMPUTADOR (PWA)
────────────────────────────────────────────────────────────────────

📌 No Google Chrome ou Microsoft Edge:

  1️⃣ Abra o endereço publicado do projeto.

  2️⃣ Aguarde o carregamento completo da página.

  3️⃣ Clique no ícone de instalação exibido na barra de endereço
      ou abra o menu do navegador.

  4️⃣ Selecione "Instalar aplicativo" ou "Instalar este site como
      aplicativo".

  5️⃣ Confirme a instalação.

✅ Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar,
   pela área de trabalho ou pelo gerenciador de aplicativos do
   sistema.


📱 7. INSTALAÇÃO NO CELULAR OU TABLET
────────────────────────────────────────────────────────────────────

📌 Em navegadores compatíveis:

  1️⃣ Abra o endereço do projeto.

  2️⃣ Acesse o menu do navegador.

  3️⃣ Selecione "Instalar aplicativo" ou "Adicionar à tela inicial".

  4️⃣ Confirme o nome e a instalação.

✅ O ícone será adicionado à tela inicial do dispositivo.


ℹ️ 8. OBSERVAÇÕES SOBRE A INSTALAÇÃO PWA
────────────────────────────────────────────────────────────────────

📌 A disponibilidade e o nome da opção de instalação podem variar
   conforme o navegador e o sistema operacional.

📌 Abrir somente o arquivo index.html pelo computador não garante a
   instalação como PWA.

📌 O projeto deve ser publicado em HTTPS para utilizar os recursos
   completos de instalação e service worker.

📌 O funcionamento offline depende da configuração do
   service-worker.js e dos arquivos adicionados ao cache.

📌 Atualizações no projeto podem exigir a atualização da versão do
   cache do service worker.


🚀 9. COMO USAR
────────────────────────────────────────────────────────────────────

🔓 Primeiro acesso
   Se nenhuma senha foi definida, o campo de senha aparece vazio.
   Basta clicar em "Entrar" para acessar.

🔑 Definir ou alterar a senha
   Abra Configurações pelo ícone de engrenagem na sidebar. Preencha
   a senha atual (vazia no primeiro uso) e a nova senha. Clique em
   "Gravar".

📂 Abrir um módulo
   Clique em um dos cartões da tela inicial ou nos ícones da sidebar.

🏠 Voltar ao início
   Clique no logo "A" no topo da sidebar.

🔒 Bloquear o sistema
   Clique no ícone de cadeado na sidebar para fazer logout e exigir
   a senha novamente.

❌ Fechar Configurações
   Clique em "Voltar" ou clique fora do painel de configurações.


🛡️ 10. SEGURANÇA E SENHA MESTRE
────────────────────────────────────────────────────────────────────

⚠️ A senha mestre é armazenada em texto puro no LocalStorage, na
   chave "senhaMaster". Isso não é criptografia forte. Trata-se
   apenas de uma barreira de acesso local.

🔍 Qualquer pessoa com acesso ao navegador e conhecimento técnico
   pode ler ou apagar o LocalStorage. Se a chave "senhaMaster" for
   removida, o sistema volta a aceitar senha vazia.

🔁 Para redefinir a senha sem saber a atual, limpe o LocalStorage
   ou utilize a função Reset Total nas Configurações.

🚫 Não utilize esta aplicação para armazenar dados sensíveis em
   ambientes compartilhados sem as devidas precauções.


📥 11. BACKUP COMPLETO
────────────────────────────────────────────────────────────────────

📍 O backup completo está disponível em Configurações > Backup
   Completo.

O processo executa as seguintes etapas:

1️⃣ Fecha o iframe do módulo ativo para liberar conexões com o
   IndexedDB.

2️⃣ Coleta todas as chaves do LocalStorage.

3️⃣ Enumera e exporta todos os bancos do IndexedDB, incluindo versão,
   object stores, índices, registros e chaves.

4️⃣ Gera um arquivo JSON com tipo, versão, data de geração, senha
   mestre, LocalStorage e IndexedDB.

5️⃣ Baixa o arquivo com o nome:
   Backup_Auditoria_<AAAA>_<DD-MM-AAAA>_<HH>h<MM>.json

💾 Recomenda-se realizar backups periódicos e guardar os arquivos em
   local seguro, como disco local, pen drive ou nuvem.


📤 12. RESTAURAÇÃO COMPLETA
────────────────────────────────────────────────────────────────────

📍 A restauração completa está disponível em Configurações >
   Restaurar Completo.

O processo solicita um arquivo JSON de backup, valida o campo "tipo"
e pede confirmação explícita antes de substituir os dados atuais.

Em seguida, fecha o iframe, restaura o LocalStorage, restaura a
senha mestre quando presente, apaga os bancos atuais do IndexedDB
e os recria a partir do backup.

Ao final, exibe um relatório com bancos restaurados, registros
gravados e falhas, e recarrega a página.

⚠️ Atenção: a restauração do IndexedDB apaga os bancos atuais antes
   de recriá-los. Certifique-se de que o arquivo de backup está
   íntegro.


🚨 13. RESET TOTAL
────────────────────────────────────────────────────────────────────

📍 O Reset Total está disponível em Configurações > RESET TOTAL
   (APAGAR TUDO).

O processo exige duas confirmações explícitas, fecha o iframe, limpa
todo o LocalStorage, apaga todos os bancos do IndexedDB quando a API
indexedDB.databases() está disponível e recarrega a página.

❌ Esta ação é irreversível. Faça backup antes de executá-la.


🗂️ 14. ESTRUTURA DE ARQUIVOS
────────────────────────────────────────────────────────────────────

📄 index.html
   Casca do sistema, com login, sidebar, tela inicial, configurações,
   backup, restauração e reset.

🖼️ icon.ico
   Favicon opcional.

🏠 Auditor de Locação.html
   Módulo de auditoria de contratos de locação.

🏡 Auditor de Compra & Venda.html
   Módulo de auditoria de contratos de compra e venda.

🔗 Os nomes dos módulos são referenciados no index.html com
   codificação URL:
      Auditor%20de%20Loca%C3%A7%C3%A3o.html
      Auditor%20de%20Compra%20%26%20Venda.html

📦 service-worker.js (opcional)
   Necessário para o funcionamento completo como PWA instalável e
   para o modo offline.


🎨 15. CUSTOMIZAÇÃO
────────────────────────────────────────────────────────────────────

➕ Adicionar um novo módulo

1️⃣ Crie o arquivo HTML do novo módulo no mesmo diretório.

2️⃣ Adicione um botão na sidebar com a chamada openModule.

3️⃣ Registre o módulo no objeto MODULES, informando a URL e o índice.

4️⃣ Opcionalmente, adicione um cartão na tela inicial com a chamada
   openModuleByName.

📌 A ordem dos índices no objeto MODULES deve corresponder à ordem
   dos botões de módulo na sidebar.

🎨 Alterar a aparência
   As variáveis CSS no :root controlam a paleta principal:
      --bg-deep, --accent e --border.

🖼️ O fundo temático é definido em .fundo-background, com imagem do
   Unsplash e gradiente. Substitua a URL para trocar a imagem.

🔤 Alterar as fontes
   As fontes são carregadas pelo Google Fonts no cabeçalho do HTML.
   Para uso offline, baixe os arquivos .woff2 e declare @font-face
   localmente.


⚖️ 16. POLÍTICA DE USO E RESPONSABILIDADE
────────────────────────────────────────────────────────────────────

A política exibida no sistema resume os seguintes pontos:

1️⃣ Armazenamento local: todos os dados ficam no navegador, em
   LocalStorage e IndexedDB. Não há servidor externo.

2️⃣ Responsabilidade pelos dados e backups: a realização de backups
   periódicos é de total e exclusiva responsabilidade do usuário.

3️⃣ Isenção de responsabilidade: o sistema, seus desenvolvedores e
   mantenedores não se responsabilizam por perda, corrupção ou
   eliminação de dados decorrentes de limpeza do navegador,
   formatação do dispositivo, falhas do sistema operacional, ação
   de antivírus ou ausência de cópias de segurança.

💾 Recomenda-se backup frequente por meio de Configurações > Backup
   Completo, salvando o arquivo em disco local, pen drive ou nuvem.


🧰 17. TECNOLOGIAS UTILIZADAS
────────────────────────────────────────────────────────────────────

🌐 HTML5 e CSS3, com variáveis CSS, gradientes e backdrop-filter.

🟨 JavaScript vanilla, sem frameworks.

💾 LocalStorage para persistência simples.

🗄️ IndexedDB para dados estruturados dos módulos.

📦 Blob e URL.createObjectURL para download de backup.

📖 FileReader para leitura de arquivos de backup.

🔤 Google Fonts: Cinzel e Montserrat.

🖼️ Imagem de fundo temática do Unsplash.

⚙️ (Opcional) service-worker.js para recursos de PWA e modo offline.


📄 18. LICENÇA
────────────────────────────────────────────────────────────────────

ℹ️ Nenhuma licença específica foi definida no arquivo fornecido.
   Antes de distribuir ou publicar o projeto, inclua uma licença
   compatível com a finalidade pretendida e verifique as licenças
   das bibliotecas externas utilizadas.


⚠️ 19. AVISO
────────────────────────────────────────────────────────────────────

📚 Este projeto é uma demonstração educacional desenvolvida para
   estudos de HTML, CSS e JavaScript.

🏢 A empresa mencionada é fictícia e qualquer semelhança com
   empresas reais é mera coincidência.

⚖️ Este sistema é uma ferramenta de apoio à análise contratual e
   não substitui a avaliação de um profissional jurídico habilitado.
   As regras implementadas nos módulos são heurísticas de conferência
   e podem não cobrir todas as nuances legais aplicáveis.


════════════════════════════════════════════════════════════════════
   Fim do README — Auditoria Contratual by Center Soft Inc.®
════════════════════════════════════════════════════════════════════
O EternalBlue é uma vulnerabilidade de execução remota de código que afeta o protocolo SMB (Server Message Block) usado pelo sistema operacional Microsoft Windows. A vulnerabilidade foi descoberta pela Agência de Segurança Nacional dos Estados Unidos (NSA) e foi exposta publicamente em abril de 2017 por um grupo de hackers conhecido como Shadow Brokers.

A vulnerabilidade permite que um invasor execute código malicioso em um sistema Windows sem autenticação ou interação do usuário. O exploit pode ser usado para espalhar rapidamente malware em toda a rede, permitindo que o invasor controle vários sistemas Windows.

O exploit funciona aproveitando uma falha na forma como o protocolo SMB lida com um pacote de mensagem conhecido como "Negotiate Protocol Request". O invasor envia um pacote especialmente criado para um serviço SMBv1 vulnerável, fazendo com que o serviço execute código malicioso que permite ao invasor assumir o controle do sistema.

A vulnerabilidade afeta várias versões do sistema operacional Windows, incluindo Windows 7, Windows 8.1, Windows 10 e Windows Server 2008, 2012 e 2016. A Microsoft lançou um patch para corrigir a vulnerabilidade, mas muitas organizações ainda não atualizaram seus sistemas, tornando-os vulneráveis a ataques usando o EternalBlue.

_____________________________________________________________________________________________________________________________________________________________________


Para escanear um sistema em busca da vulnerabilidade EternalBlue usando o Nmap, você pode executar o seguinte comando no prompt de comando:

 # nmap -p445 --script smb-vuln-ms17-010 <ip_alvo>
 
 _____________________________________________________________________________________________________________________________________________________________________
 
Uma vez identificado o sistema vulnerável, é possível testar a vulnerabilidade usando um exploit disponível no Metasploit Framework. Você pode usar o módulo "windows/smb/ms17_010_eternalblue" do Metasploit para testar a vulnerabilidade. Antes de executar o exploit, você deve configurar o endereço IP e a porta do sistema alvo.

Inicie o Metasploit Framework: Abra o console do Metasploit Framework e aguarde até que ele seja inicializado.

Selecionar o exploit: Use o comando search para pesquisar a vulnerabilidade que deseja explorar. Por exemplo, para procurar exploits para a vulnerabilidade EternalBlue no Windows, use o comando search EternalBlue.

Configurar o exploit: Use o comando use para selecionar o exploit específico que deseja usar. Por exemplo, use o comando use windows/smb/ms17_010_eternalblue para selecionar o exploit para a vulnerabilidade EternalBlue no Windows.

Configurar as opções do exploit: Use o comando show options para ver as opções disponíveis para o exploit selecionado. Configure as opções necessárias, como o endereço IP e a porta do sistema alvo.

Executar o exploit: Use o comando exploit para executar o exploit. Se tudo correr bem, o Metasploit deve conseguir explorar a vulnerabilidade e obter acesso ao sistema alvo.

by hackealy >.<

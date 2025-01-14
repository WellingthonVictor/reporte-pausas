
O código implementa um monitoramento contínuo de operações em um sistema online, realizando as seguintes funções principais:

Login e Navegação no Sistema:

Efetua login em um site para capturar dados de operações usando o navegador Microsoft Edge, configurado com o WebDriver do Selenium.
Coleta e Processamento de Dados:

Extrai informações de agentes online, como o número de agentes disponíveis, em pausa, ocupados, ou não prontos.
Ajusta os números para desconsiderar agentes em treinamento ou operadores específicos (com IDs fixos).
Armazenamento de Dados:

Salva os dados coletados em um arquivo Excel, adicionando-os a uma tabela organizada, criando o arquivo se ele ainda não existir.
Envio de Relatórios para o Teams:

Com base na proporção de agentes em pausa, o código decide se a operação está em ordem (pausa ≤ 25%) ou em risco de abandono (pausa > 25%).
Envia mensagens para chats específicos no Microsoft Teams, incluindo texto descritivo e, em alguns casos, capturas de tela da tabela de monitoramento.
Automação e Loop Contínuo:

Executa verificações periódicas entre 8h e 23h59, com pausas de 9 minutos entre cada iteração, ajustando-se para evitar execuções em horários fora do intervalo definido.
Gerenciamento de Erros:

Implementa tratativas para situações como falha de login, problemas de navegação, ou ausência de elementos esperados na página.

# consulta_ips
Robo de consulta de ips

Dica de utilizade Geral.

Neste projeto, a robotização se resume em copiar de uma lugar e colar em outro. 
Pode ser utilizado para obter informações onde não temos acesso ao banco de dados ou para upar, imputar/inserir informações em um sistema manualmente. 

Neste caso em especifico, tinhamos alguns circuitos para consultar seus respectivos ip's, consultamos um por um pois éra a unica ferramenta que tinhamos acesso, então o processo precisava ser realizado dessa forma. 

Outra situação real de uso:
Temos uma ferramenta chamada: REDETELECOM, onde é o cadastro oficial dos ip's dos modens, onde uma pessoa de determinada equipe faz a insersão manualmente um a um no momento que estão disponiveis. Corriqueiramente, essa atividade não tinha sido feita por falta de recursos (tempo), então modem saia para campo sem cadastro na ferramenta, impactanto o tempo de atividade do tecnico que teria que ligar para fazer a consulta ip, ação que não aconteceria caso o robo tivesse feito a atividade.  Nesse cenário, esse robo poderia fazer essa atividade sozinho.

Vantagens da utiliazação de robos:
    * Não comete erros de digitação.
    * Não comete erros de click em lugares errados.
    * Não comete erros operacionais.
    * Não insere dados errados. 
    * Não deleta dados equivocadamete. 
    * Economiza tempo de mão de obra. 


Utilizamos os comandos do Pyautogui e Time para realização desse projeto.


Aqui estão os comandos do PyAutoGUI para as funções que você mencionou:
1. Click (Clique Simples)

pyautogui.click(x=100, y=200)  # Clica na posição (100, 200)

Se quiser clicar onde o mouse está atualmente:

pyautogui.click()

2. DoubleClick (Clique Duplo)

pyautogui.doubleClick(x=100, y=200)  # Clique duplo na posição (100, 200)

Ou onde o mouse está:

pyautogui.doubleClick()

3. time.sleep (Pausa)

time.sleep(2)  # Pausa por 2 segundos

4. typewrite (Digitar Texto)

pyautogui.typewrite("Olá, mundo!", interval=0.1)  # Digita com 0.1s de intervalo entre caracteres

5. hotkey (Atalhos de Teclado), para clicar em duas teclas juntas:

pyautogui.hotkey('ctrl', 'c')  # Pressiona Ctrl+C (Copiar)
pyautogui.hotkey('ctrl', 'v')  # Pressiona Ctrl+V (Colar)
pyautogui.hotkey('alt', 'tab')  # Alterna entre janelas

6. Pegar a Posição do Clique

Para descobrir onde está o cursor do mouse:

x, y = pyautogui.position()
print(f"Posição do mouse: {x}, {y}")

Ou para exibir em tempo real:

while True:
    print(pyautogui.position())
    time.sleep(1)  # Atualiza a posição a cada 1 segundo


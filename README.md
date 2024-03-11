import pyautogui  
import time
pyautogui.press('Win')
time.sleep(1.5)
pyautogui.write('Google')
time.sleep(2)
pyautogui.press('enter')
time.sleep(2)
link = "https://dlp.hashtagtreinamentos.com/python/intensivao/login"
pyautogui.write(link)
time.sleep(1)
pyautogui.press("enter")
time.sleep(1)
pyautogui.press('tab')
pyautogui.write('guurodriguess3@gmail.com')
pyautogui.press('tab')
pyautogui.write('20354734')
pyautogui.press('tab')
pyautogui.press('Enter')


import pandas
tabela = pandas.read_csv("produtos.csv")
print(tabela)

for linha in tabela.index:
    
    codigo = tabela.loc[1, "codigo"]
    pyautogui.write(codigo)
    pyautogui.press('tab')

    marca = tabela.loc[linha, "marca"]
    pyautogui.write(marca)
    pyautogui.press('tab')

    tipo = tabela.loc[linha, "tipo"]
    pyautogui.write(tipo)
    pyautogui.press('tab')
    
    categoria = tabela.loc[linha, "categoria"]
    pyautogui.write(str((categoria)))
    pyautogui.press('tab')

    preco_unitario = tabela.loc[linha, "preco_unitario"]
    pyautogui.write(str(preco_unitario))
    pyautogui.press('tab')
    
    custo = tabela.loc[linha, "custo"]
    pyautogui.write(str(custo))
    pyautogui.press('tab')

    obs = tabela.loc[linha, "obs"]
    if not pandas.isna(obs):
         pyautogui.write(obs)
    pyautogui.press('tab')

    pyautogui.press('tab')
    pyautogui.press('enter')
    pyautogui.press('f5')
    

# registro_por_registro

import sqlite3
conexao = sqlite3.connect("agenda.db")
cursor = conexao.cursor()
cursor.execute("select * from agenda")
while True:
  resultado = cursor.fetchall()
  if resultado is None:
    print(f"Nome: {registro[0]}\nTelefone: {registro[1]}")
cursor.close()
conexao.close()

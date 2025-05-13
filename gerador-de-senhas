import tkinter as tk
import random
import string

def generate_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    while True:
        password = ''.join(random.choice(characters) for i in range(length))
        if (any(c.islower() for c in password) and
            any(c.isupper() for c in password) and
            any(c.isdigit() for c in password) and
            any(c in string.punctuation for c in password)):
            break
    password_entry.delete(0, tk.END)
    password_entry.insert(0, password)
    root.clipboard_clear()
    root.clipboard_append(password)
    copied_label.config(text="Senha copiada!")

def copy_password():
    password = password_entry.get()
    root.clipboard_clear()
    root.clipboard_append(password)
    copied_label.config(text="Senha copiada!")

def on_option_change():
    selected_option = option_var.get()
    length = int(selected_option.split('-')[1].strip().split()[0])
    generate_password(length)

# Tela principal
root = tk.Tk()
root.title("Gerador de Senhas Seguras")

# Opções
option_var = tk.StringVar(value="Escolha a quantidade de dígitos")
options = [
    "A - 12 dígitos", "B - 13 dígitos", "C - 14 dígitos",
    "D - 15 dígitos", "E - 16 dígitos", "F - 17 dígitos", "G - 18 dígitos"
]
option_menu = tk.OptionMenu(root, option_var, *options)
option_menu.pack(pady=5)
 
# Mostra senha
password_label = tk.Label(root, text="Senha Gerada:")
password_label.pack(pady=5)

password_entry = tk.Entry(root, width=50)
password_entry.pack(pady=5)

# Botão gera senha
generate_button = tk.Button(root, text="Gerar Senha", command=on_option_change)
generate_button.pack(pady=10)

# Botão copiar senha
copy_button = tk.Button(root, text="Copiar Senha", command=copy_password)
copy_button.pack(pady=5)

copied_label = tk.Label(root, text="")
copied_label.pack(pady=5)

root.mainloop()

import smtplib

enviar_email = input(str("Digite seu email: "))

rec_email = "pessoa que vai receber"

senha_email = input(str("Digite sua senha:"))

subject = str(input("Digite oque voce fez: "))

server = smtplib.SMTP('smtp.gmail.com', 587)

server.starttls()

server.login(enviar_email, senha_email)

print("Logado com sucesso")

server.sendmail(enviar_email, rec_email, subject)

print("Email enviado para ", rec_email)

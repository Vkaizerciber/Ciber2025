# Ciber2025
 Ataque de Força Bruta com Medusa e Kali Linux
Objetivo: Simular um ataque de força bruta em um ambiente vulnerável (Metasploitable 2 e DVWA) utilizando a ferramenta Medusa e Kali Linux, e exercitar medidas de prevenção.

Requisitos:

- Kali Linux instalado e configurado
- Metasploitable 2 instalado e configurado
- DVWA (Damn Vulnerable Web Application) instalado e configurado
- Medusa instalado e configurado no Kali Linux

Passos:

1. Configurar o ambiente:
- Configurar a rede do Kali Linux e do Metasploitable 2 para estarem na mesma sub-rede.
- Configurar o DVWA para estar acessível a partir do Kali Linux.
- Verificar se o Kali Linux e o Metasploitable 2 estão conectados à mesma rede.
- Verificar se o DVWA está funcionando corretamente e acessível a partir do Kali Linux.

2. Instalar e configurar Medusa:
- Instalar Medusa no Kali Linux: apt-get install medusa
- Configurar Medusa para utilizar a wordlist de senhas desejada.
- Criar uma wordlist de senhas personalizada ou utilizar uma existente.
- Configurar Medusa para utilizar a wordlist de senhas criada.

3. Simular ataque de força bruta:
- Utilizar Medusa para realizar um ataque de força bruta no Metasploitable 2:
- medusa -h <IP do Metasploitable 2> -u <usuário> -P <wordlist de senhas> -M ftp
- Utilizar Medusa para realizar um ataque de força bruta no DVWA:
- medusa -h <IP do DVWA> -u <usuário> -P <wordlist de senhas> -M http -m DIR:/dvwa/login.php
- Analisar os resultados do ataque e identificar as vulnerabilidades encontradas.

4. Documentar os resultados:
- Documentar os comandos utilizados e os resultados obtidos.
- Analisar os resultados e identificar as vulnerabilidades encontradas.
- Documentar as medidas de prevenção que podem ser tomadas para evitar ataques de força bruta.

5. Exercitar medidas de prevenção:
- Configurar o Metasploitable 2 e o DVWA para utilizar senhas fortes e únicas.
- Configurar o firewall do Metasploitable 2 e do DVWA para bloquear tentativas de conexão suspeitas.
- Utilizar um sistema de detecção de intrusão (IDS) para monitorar a rede e detectar ataques de força bruta.

Comandos úteis:

- medusa -h <IP> -u <usuário> -P <wordlist de senhas> -M <módulo>
- medusa -h <IP> -u <usuário> -P <wordlist de senhas> -M ftp
- medusa -h <IP> -u <usuário> -P <wordlist de senhas> -M http -m DIR:/dvwa/login.php

Wordlists de senhas:

- rockyou.txt
- wordlist.txt
- passwords.txt

Módulos do Medusa:

- ftp
- http
- ssh
- smb

Díficas e Desafios:

- Configurar o ambiente e as ferramentas corretamente.
- Encontrar e utilizar uma wordlist de senhas eficaz.
- Analisar os resultados e identificar as vulnerabilidades encontradas.
- Implementar medidas de prevenção eficazes.

Recursos adicionais:
Testando o ataque de força bruta:

1. Configurar o ambiente:
- Certifique-se de que o Kali Linux e o Metasploitable 2 estão conectados à mesma rede.
- Certifique-se de que o DVWA está funcionando corretamente e acessível a partir do Kali Linux.
2. Instalar e configurar Medusa:
- Instale Medusa no Kali Linux: apt-get install medusa
- Crie uma wordlist de senhas personalizada ou utilize uma existente.
- Configure Medusa para utilizar a wordlist de senhas criada.
3. Simular ataque de força bruta:
- Utilize Medusa para realizar um ataque de força bruta no Metasploitable 2:
- medusa -h <IP do Metasploitable 2> -u msfadmin -P /usr/share/wordlists/rockyou.txt -M ftp
- Utilize Medusa para realizar um ataque de força bruta no DVWA:
- medusa -h <IP do DVWA> -u admin -P /usr/share/wordlists/rockyou.txt -M http -m DIR:/dvwa/login.php
4. Analisar os resultados:
- Verifique os resultados do ataque e identifique as vulnerabilidades encontradas.

Exemplo de saída:


medusa -h 192.168.1.100 -u msfadmin -P /usr/share/wordlists/rockyou.txt -M ftp
Medusa v2.2 [http://www.thycotic.com]
Copyright (c) 2023 Thycotic Software Ltd.
FTP Host: 192.168.1.100
FTP User: msfadmin
FTP Password: msfadmin


Observação:

- O ataque de força bruta pode levar algum tempo para ser concluído, dependendo da velocidade da rede e da complexidade da wordlist de senhas.
- É importante lembrar que o ataque de força bruta é ilegal se não for autorizado pelo proprietário do sistema.
- É recomendável utilizar este tipo de ataque apenas em ambientes de teste e com a permissão do proprietário do sistema.
- Documentação oficial do Medusa: https://www.thycotic.com/products/medusa/
- Documentação oficial do Metasploitable 2: https://metasploit.help.rapid7.com/docs/metasploitable-2
- Documentação oficial do DVWA: https://dvwa.co.uk/

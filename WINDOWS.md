# Configurando SSH no Windows


### 1- Precisamos gerar uma chave SSH que seu computador vai usar pra se autorizar com o Github. Digite o seguinte comando no Git Bash:

  `ssh-keygen -t rsa -b 4096 -C "seu_email@dominio.com" (lembre-se de trocar o e-mail)`


### O resultado será:

<pre>
  Generating public/private rsa key pair.  
  Enter file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]  
  Você quer salvar a chave nesse arquivo mesmo, só dê enter.
</pre>

### Depois, ele vai pedir uma senha:

<pre>
  Enter passphrase (empty for no passphrase): [Type a passphrase]  
  Enter same passphrase again: [Type passphrase again]  
</pre>

Essa senha você vai ter que digitar toda vez que for baixar algo de um repositório ou enviar algo pra lá. Eu deixo sem mesmo.
Se quiser deixar sem, só dê enter. Se não, coloque a senha e confirme.

Em seguida, você verá uma mensagem dizendo que deu tudo certo:

`Your identification has been saved in /Users/you/.ssh/id_rsa.`

<pre>
# Your public key has been saved in /Users/you/.ssh/id_rsa.pub.
# The key fingerprint is:
# 01:0f:f4:3b:ca:85:d6:17:a1:7d:f0:68:9d:f0:a2:db seuemail@dominio.com
</pre>


###  2- Agora, precisamos adicionar a chave que criamos ao ssh-agent. Primeiro, vamos ativa-lo:

  `eval $(ssh-agent -s)`  
Em seguida, vamos adicionar a chave que geramos ao ssh-agent:

  `ssh-add ~/.ssh/id_rsa`

###  3- Agora, vamos associar a chave que geramos à nossa conta do Github.
Para copiar a chave do bash, digite o seguinte comando:

  `clip < ~/.ssh/id_rsa.pub` 

A chave agora está no nosso ctrl+v :P

### Agora adicione ao seu Github



# Professor Douglas Morais
## GamaAcademy
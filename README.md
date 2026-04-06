# Introdução

## Inicialização

### 1. Ligar o Access Point

Certifique-se de possuir:
- Um _access point_ (de preferência aquele na qual o aplicativo está configurado)
- Um alimentador para o _access point_
- 2 cabos ethernets

![Itens access point][Itens-access-point]

Conecte um dos cabos ethernet na entrada _PoE_ do _access point_ e na respectiva entrada:

![Cabo de alimentação no AP][Cabo-de-alimentação-no-AP]
![Cabo de alimentação ligada ao alimentador do AP][Cabo-de-alimentação-ligada-ao-alimentador-do-AP]

Em seguida, conecte o outro cabo ethernet na entrada LAN do alimentador e a outra extremidade numa porta de rede ethernet:

![Cabo LAN no alimentador][Cabo-LAN-no-alimentador]
![Cabo LAN ligada a uma porta de rede ethernet][Cabo-LAN-ligada-a-uma-porta-de-rede-ethernet]

Assim ficará se o _access point_ estiver ligado:

![Access point ligado][Access-point-ligado]

**PS.:** não preciso dizer que o alimentador deve estar conectado a uma tomada capaz de ligá-lo, certo?

> [!NOTE]
> O _access point_ não é obrigatório, mas garante um endereço de IP constante.

### 2. Ligar o carrinho

Pressione o botão _switch_, se as baterías estiverem carregadas, idealmente, o _raspberry pi_ ligará:

![Raspberry Pi ligado][Raspberry-Pi-ligado]

O _raspberry pi_ foi programado para executar um [servidor][Backend] ao iniciar.

### 3. Baixar o Aplicativo do Projeto

Acesse o seguinte link e biaxe o repositório: [https://github.com/labtec-satc/RoboCar.git][Git]

Caso tenha Git instalado em sua máquina, abra o terminal e execute o seguinte comando:

```
git clone https://github.com/labtec-satc/RoboCar.git
```

O arquivo baixado é o repositório do projeto. Nele há o aplicativo _web_ que se conectará ao servidor presente no _raspberry pi_.

### 4. Conectar-se a Mesma Rede do Carrinho

O _access point_ gerará uma rede _Wi-Fi_, na qual o _raspbery pi_ se conectará. Para o aplicativo _web_ se comunicar com o servidor é necessário que ambos, o _raspberry pi_ e a máquina com o aplicativo, estejam conectados na mesma rede.

#### Wi-Fi
- **Nome:** SATC_LABTEC 
- **Senha:** labtec2025

![Rede Labtec][Rede-Labtec]

> [!NOTE]
> Uma conexão com outra rede não proveniente do _access point_, próprio para o projeto, pode ser realizada, porém configurações nos códigos do projeto podem ser necessárias.

### 5. Executar o Aplicativo

> [!NOTE]
> Para prosseguir é necessário possuir um gerenciador de pacotes, como o _node_, instalado.

Entre na pasta com os arquivos do aplicativo:
```
cd RoboCar\Frontend\carro_remoto
```

Instale as dependências do _node_:
```
npm install
```

Execute o aplicativo _web_:
```
npm run dev
```

Se tudo ocorreu como o idealizado, o terminal mostrará algo parecido com:

![Aplicativo executado][exec-app]

### 6. Pé na Tábua

Meu presente de despedidad é a seguinte "pérola":

<img src="./Exemplos/carro-mov.gif" height=350/>

<!-- Links -->
[Itens-access-point]: ./Exemplos/itens-ap.jpg
[Cabo-de-alimentação-no-AP]: ./Exemplos/conexao-ap1.jpg
[Cabo-de-alimentação-ligada-ao-alimentador-do-AP]: ./Exemplos/conexao-ap2.jpg
[Cabo-LAN-no-alimentador]: ./Exemplos/conexao-ap3.jpg
[Cabo-LAN-ligada-a-uma-porta-de-rede-ethernet]: ./Exemplos/conexao-ap4.jpg
[Access-point-ligado]: ./Exemplos/ligado-rot.jpg
[Raspberry-Pi-ligado]: ./Exemplos/ligado-car.jpg
[Backend]: ./Backend/
[Git]: https://github.com/labtec-satc/RoboCar.git
[Rede-Labtec]: ./Exemplos/conexao-rede.jpg
[exec-app]: ./Exemplos/exec-app.jpg
[carro-mov]: ./Exemplos/carro-mov.gif
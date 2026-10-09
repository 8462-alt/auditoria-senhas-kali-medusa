# Notas de laboratório e comandos

Use este arquivo para registrar comandos, contexto e resultados
**somente no seu laboratório autorizado**. Os exemplos abaixo são
voltados à configuração e ao reconhecimento básico; não representam
evidência de que os testes foram executados.

## 1. Verificar a interface de rede no Kali

``` bash
ip addr
ip route
```

Registre qual interface está conectada à rede isolada do laboratório.

## 2. Verificar conectividade com o alvo

Substitua `IP_DO_ALVO` pelo endereço privado da VM de treinamento:

``` bash
ping -c 4 IP_DO_ALVO
```

Se o alvo não responder, isso não prova que está desligado; o ICMP pode
estar bloqueado.

## 3. Reconhecimento básico com Nmap

Somente no alvo de laboratório autorizado:

``` bash
nmap -sV IP_DO_ALVO
```

Registre a data, o endereço de laboratório e os serviços encontrados.
Não escaneie endereços públicos ou dispositivos de terceiros.

## 4. Medusa e autenticação

Antes de qualquer teste, confirme que o serviço pertence ao laboratório,
que as contas são fictícias e que o escopo foi autorizado. Defina um
limite baixo de tentativas e interrompa o teste se houver comportamento
inesperado. Documente a configuração usada na aula, sem incluir senhas
reais.

## Modelo de registro

-   Data e hora:
-   VM de origem:
-   VM alvo:
-   Serviço avaliado:
-   Objetivo:
-   Limite de tentativas:
-   Resultado observado:
-   Evidência:
-   Mitigação recomendada:

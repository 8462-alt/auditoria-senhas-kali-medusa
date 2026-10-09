# Auditoria de Senhas com Kali Linux e Medusa

> **Projeto educacional de cibersegurança.** Os testes descritos neste
> repositório devem ocorrer exclusivamente em máquinas próprias ou
> ambientes com autorização explícita. Não use as técnicas contra
> sistemas públicos, redes de terceiros ou contas reais.

## Objetivo

Documentar o estudo de auditoria de autenticação e dos riscos de senhas
fracas, usando um laboratório isolado com Kali Linux e uma máquina
vulnerável de treinamento. O projeto aborda conceitos de força bruta,
password spraying, enumeração de serviços e medidas de mitigação.

## Escopo e ambiente

-   **Kali Linux:** máquina usada para estudar ferramentas de auditoria.
-   **Metasploitable 2:** alvo de treinamento intencionalmente
    vulnerável.
-   **DVWA:** aplicação web deliberadamente vulnerável para estudo.
-   **VirtualBox:** virtualização das máquinas.
-   **Medusa e Nmap:** ferramentas estudadas no contexto de auditoria
    autorizada.

Configure as VMs em uma rede isolada de laboratório. Não exponha o
Metasploitable 2 ou o DVWA à internet nem à rede doméstica. Tire um
snapshot antes dos testes e use somente contas fictícias.

## Cenários de estudo

### 1. Reconhecimento de serviços

Identificar quais serviços estão ativos no alvo de laboratório e
registrar apenas os serviços necessários ao exercício. Anote o endereço
IP privado do alvo, a data do teste e a configuração de rede.

### 2. FTP

Estudar como senhas fracas podem permitir autenticação indevida em um
serviço FTP. Registre o método de teste, a conta fictícia usada e o
resultado observado. Não inclua credenciais reais.

### 3. Formulário web (DVWA)

Estudar os riscos de tentativas repetidas de login em uma aplicação de
treinamento. Registre se há limitação de tentativas, mensagens de erro
informativas ou outros controles de proteção.

### 4. SMB e password spraying

Estudar conceitualmente como o password spraying testa uma senha comum
em várias contas e por que isso pode gerar bloqueios ou alertas. Faça
qualquer teste prático apenas com contas fictícias e dentro de um escopo
autorizado, evitando tentativas em massa.

## Resultados

**Preencha esta seção somente depois de executar os testes.** Não
declare sucesso ou vulnerabilidades sem evidências.

  Cenário                      Resultado observado   Evidência
  ---------------------------- --------------------- -----------
  Reconhecimento de serviços   A preencher           `images/`
  FTP                          A preencher           `images/`
  DVWA                         A preencher           `images/`
  SMB                          A preencher           `images/`

## Recomendações de mitigação

-   Usar senhas longas, exclusivas e não previsíveis.
-   Ativar MFA sempre que disponível.
-   Aplicar limitação de tentativas, atrasos progressivos e alertas para
    falhas repetidas.
-   Evitar mensagens de login que revelem se o usuário existe.
-   Desativar serviços desnecessários e restringir o acesso por
    firewall.
-   Preferir protocolos seguros e desabilitar autenticação insegura
    quando possível.
-   Monitorar logs de autenticação e investigar padrões anormais.
-   Revisar permissões e remover contas desnecessárias.

## Evidências e privacidade

Coloque capturas de tela não sensíveis na pasta `images/`. Oculte nomes
de usuário pessoais, endereços públicos, tokens, senhas e quaisquer
dados de terceiros. Use apenas dados fictícios.

## Conclusão

Este repositório serve como documentação de aprendizagem sobre riscos de
autenticação e controles defensivos. Os resultados finais devem refletir
somente o que foi realmente observado no laboratório.

## Referências

-   [Kali Linux](https://www.kali.org/)
-   [Medusa](http://www.foofus.net/jmk/medusa/medusa.html)
-   [Nmap Reference Guide](https://nmap.org/book/)
-   [DVWA](https://github.com/digininja/DVWA)
-   [Metasploitable
    2](https://docs.rapid7.com/metasploit/metasploitable-2/)

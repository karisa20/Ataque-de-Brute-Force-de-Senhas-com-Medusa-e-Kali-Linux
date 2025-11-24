---

# **Projeto Prático de Cibersegurança**

## Ataques de Força Bruta com Kali Linux, Medusa e Ambientes Vulneráveis

Este repositório apresenta um laboratório prático de cibersegurança desenvolvido como parte do desafio da **Digital Innovation One (DIO)**.
O objetivo é **simular ataques de força bruta** em diferentes serviços, entender seu funcionamento interno e documentar técnicas, aprendizados e formas de mitigação — tudo dentro de um **ambiente seguro e controlado**.

---

## **Sobre o Projeto**

Este projeto recria cenários reais de segurança ofensiva utilizando:

* **Kali Linux** → Máquina atacante
* **Metasploitable 2** → Máquina propositalmente vulnerável
* **DVWA (Damn Vulnerable Web Application)** → Aplicação web vulnerável (opcional)

As máquinas foram configuradas no **VirtualBox**, utilizando rede **“Host-Only”**, garantindo **isolamento total** e segurança para os testes.

---

## **Objetivos do Desafio**

Ao final deste projeto, você será capaz de:

* Compreender ataques de **força bruta** em protocolos e serviços distintos (FTP, Web Forms e SMB)
* Utilizar o **Kali Linux** e a ferramenta **Medusa** para auditoria de segurança
* Documentar testes técnicos de maneira clara e estruturada
* Identificar vulnerabilidades comuns e propor medidas de mitigação
* Utilizar o **GitHub como portfólio** técnico para registrar sua jornada de aprendizado

---

## **Configuração do Ambiente**

As máquinas virtuais utilizadas foram:

### Kali Linux (Atacante)

* Ferramentas utilizadas:

  * `medusa`
  * `hydra` (opcional, para comparação)
  * Wordlists personalizadas
  * Ferramentas de enumeração (como `enum4linux-ng`)

### Metasploitable 2 (Alvo)

* Serviços vulneráveis explorados:

  * FTP
  * SMB
  * Web apps vulneráveis (DVWA quando configurado)

### DVWA – Damn Vulnerable Web Application (Opcional)

* Usada para login bruteforce automatizado em formulários web

### Rede

* **Host-Only (VirtualBox)**
* Totalmente isolada do ambiente real

---

## **Cenários Práticos Desenvolvidos**

### 1. Ataque de Força Bruta em FTP

* Enumeração do serviço
* Criação e uso de wordlist simples
* Execução do brute force com Medusa
* Validação de credenciais encontradas

### 2. Automação de Força Bruta em Formulário Web (DVWA)

* Teste em modo *Low Security*
* Análise do fluxo de requisição (POST)
* Disparo automatizado de tentativas

### 3. Password Spraying em SMB com Enumeração de Usuários

* Coleta de possíveis usuários
* Tentativas distribuídas evitando lockout
* Acesso validado manualmente

---

## **Documentação Incluída no Projeto**

Este repositório contém:

* **README.md** (este arquivo)
* Wordlists simples criadas manualmente (`/wordlists`)
* Arquivos com os comandos utilizados (`/commands`)
* Prints (`/images`)
  
---

## **Como Reproduzir o Laboratório**

1. Instale o **VirtualBox**
2. Importe as VMs do Kali e do Metasploitable
3. Configure ambas em **rede Host-Only**
4. Confirme a comunicação via `ping`
5. Execute os testes seguindo a documentação deste repositório

---

## **Mitigações e Boas Práticas Estudadas**

O projeto enfatiza medidas de segurança como:

* Implementar políticas de senha forte
* Adotar bloqueio temporário após tentativas falhas
* Habilitar autenticação multifator
* Minimizar exposição de serviços
* Monitorar logs de autenticação
* Utilizar IDS/IPS para detectar padrões de brute force

---

## **Por que este projeto importa?**

Este laboratório mostra, na prática:

* Como ataques de força bruta realmente funcionam
* Como ferramentas como Medusa se comportam
* Como analisar respostas dos serviços atacados
* Como documentar procedimentos ofensivos com responsabilidade
* Como aplicar medidas de defesa no mundo real

---

## **Aviso Legal**

> Este projeto foi realizado **exclusivamente** em ambiente controlado.
> Nunca execute varreduras, testes ou ataques em sistemas para os quais você não possua autorização explícita.

---

## **Contribuições**

Sugestões, melhorias e pull requests são sempre bem-vindos!
Sinta-se à vontade para contribuir com novas ferramentas, testes e estudos.

---

## **Se este projeto te ajudou, considere deixar uma estrela!**

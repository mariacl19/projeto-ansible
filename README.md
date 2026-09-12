# 🚀 Ambiente Virtualizado com Vagrant e Ansible

Projeto desenvolvido durante meus estudos de **Infraestrutura, Virtualização e Automação**, utilizando **Vagrant** para criação e gerenciamento de máquinas virtuais e **Ansible** para configuração dos servidores.

O objetivo do projeto é criar um ambiente virtualizado de forma automatizada, preparando uma máquina virtual para funcionar como **servidor web**.

---

## 🛠️ Tecnologias utilizadas

* 🖥️ **Vagrant** — criação e gerenciamento das máquinas virtuais
* 📦 **VirtualBox** — provedor de virtualização
* ⚙️ **Ansible** — automação e configuração do servidor
* 🌐 **Servidor Web** — configuração de uma máquina virtual para disponibilizar um serviço web
* 🐧 **Linux** — sistema utilizado no ambiente virtualizado

---

## 📂 Estrutura do projeto

```text
.
├── Vagrantfile
├── vm-ansible/
├── servidor-web/
├── hosts.ini
└── chave_privada
```

### 📄 Principais arquivos

| Arquivo/Pasta   | Descrição                                                             |
| --------------- | --------------------------------------------------------------------- |
| `Vagrantfile`   | Arquivo responsável pela configuração e criação das máquinas virtuais |
| `vm-ansible/`   | Diretório relacionado à configuração da máquina virtual com Ansible   |
| `servidor-web/` | Configurações relacionadas ao servidor web                            |
| `hosts.ini`     | Arquivo de inventário utilizado pelo Ansible                          |
| `chave_privada` | Chave utilizada para autenticação SSH no ambiente virtual             |

---

## ⚙️ Como funciona

O projeto utiliza o **Vagrant** para criar o ambiente virtualizado e o **Ansible** para automatizar a configuração das máquinas.

O fluxo básico é:

```text
Vagrant
   │
   ▼
Criação da Máquina Virtual
   │
   ▼
Configuração de Rede e SSH
   │
   ▼
Ansible
   │
   ▼
Configuração do Servidor
   │
   ▼
Servidor Web
```

Dessa forma, o ambiente pode ser recriado de maneira mais rápida e consistente, sem a necessidade de realizar todas as configurações manualmente.

---

## 🚀 Como executar o projeto

### 1. Pré-requisitos

Antes de iniciar, é necessário ter instalado:

* [Vagrant](https://developer.hashicorp.com/vagrant)
* [VirtualBox](https://www.virtualbox.org/)
* [Ansible](https://docs.ansible.com/) *(caso a configuração seja executada diretamente pelo host)*

### 2. Clone o repositório

```bash
git clone https://github.com/mariacl19/NOME-DO-REPOSITORIO.git
cd NOME-DO-REPOSITORIO
```

### 3. Inicie as máquinas virtuais

```bash
vagrant up
```

O Vagrant irá criar e iniciar as máquinas definidas no `Vagrantfile`.

### 4. Verifique o status

```bash
vagrant status
```

### 5. Acesse a máquina virtual

```bash
vagrant ssh
```

---

## 🤖 Configuração com Ansible

O arquivo `hosts.ini` é utilizado como inventário para indicar ao Ansible quais máquinas devem ser configuradas.

Exemplo:

```ini
[servidores]
servidor-web
```

A partir do inventário, o Ansible pode executar as configurações necessárias no ambiente.

Exemplo de comando:

```bash
ansible-playbook -i hosts.ini playbook.yml
```

> Os comandos podem variar de acordo com a estrutura final dos arquivos do projeto.

---

## 🌐 Servidor Web

Uma das etapas do projeto consiste na preparação de uma máquina virtual para atuar como **servidor web**.

A ideia é automatizar a configuração do ambiente, permitindo que o servidor seja criado e configurado de forma reproduzível.

---

## 📚 O que aprendi

Com este projeto, pratiquei conceitos importantes de infraestrutura e automação, como:

* Virtualização de ambientes;
* Criação e gerenciamento de máquinas virtuais;
* Utilização do Vagrant;
* Configuração de ambientes Linux;
* Acesso remoto utilizando SSH;
* Inventário do Ansible;
* Automação de configurações com Ansible;
* Configuração de servidores;
* Conceitos básicos de servidores web;
* Organização e documentação de projetos no GitHub.

---

## 🎯 Objetivo do projeto

Este projeto faz parte da minha jornada de estudos em **Tecnologia da Informação**, com foco no desenvolvimento de conhecimentos em **Infraestrutura, Linux, Virtualização, Automação e DevOps**.

A proposta é transformar configurações que seriam realizadas manualmente em processos automatizados e reproduzíveis.

---

## 👩‍💻 Autora

**Maria Clara**

Estudante de Tecnologia da Informação, interessada em desenvolvimento, infraestrutura, automação e tecnologias relacionadas à área de **DevOps**.

🔗 **GitHub:** [@mariacl19](https://github.com/mariacl19)

---

⭐ Se este projeto foi útil para você, considere deixar uma estrela no repositório!

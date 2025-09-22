# Cenaflix 🎬🎧

O **Cenaflix** é um sistema acadêmico em **Java** inspirado em plataformas de streaming, evoluindo em **dois módulos**:

1) **Cenaflix (Filmes)** — projeto **NetBeans/Ant + MySQL** para **cadastro, consulta e atualização** de filmes.  
2) **Cenaflix JPA (Podcasts & Usuários)** — projeto **Maven + JPA** para **podcasts**, **usuários** e fluxo de **login**.

<p align="left">
  <img alt="Java" src="https://img.shields.io/badge/Java-8%2B-orange">
  <img alt="Build" src="https://img.shields.io/badge/build-Ant%20%26%20Maven-blue">
  <img alt="DB" src="https://img.shields.io/badge/DB-MySQL-informational">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-success">
</p>

---

## ✨ Funcionalidades
### 🎬 Módulo Filmes (NetBeans/Ant + MySQL)
- Cadastro de filmes
- Consulta/listagem de catálogo
- Atualização de registros
- Interface Swing

### 🎧 Módulo Podcasts & Usuários (Maven + JPA)
- Cadastro e listagem de podcasts
- Cadastro/gerenciamento de usuários
- Tela de login e menu inicial
- Persistência via JPA (`persistence.xml`)

---

## 🧰 Tecnologias
- Java 8+ (POO, Swing)
- MySQL (JDBC / JPA)
- NetBeans/Ant (Filmes)
- Maven + JPA (Podcasts/Usuários)
- Padrões: DAO/DTO

---

## ⚙️ Como executar

> **Dica:** publique quaisquer **.zip/.jar** em **Releases**; mantenha o **código-fonte descompactado** no repositório para melhor visualização.

### 1) Pré-requisitos
- **Java 8+**
- **MySQL** em execução (`localhost`)
- IDE (NetBeans recomendado para módulo Ant)

### 2) Módulo Filmes (Ant + MySQL)
- Importe o projeto **Cenaflix** no NetBeans.
- Execute o script SQL do banco (ex.: `BDCenaflix.sql`).
- Ajuste as credenciais JDBC no DAO (ex.: `FilmesDAO.java`).
- Compile e execute (menu e telas Swing).

### 3) Módulo Podcasts & Usuários (Maven + JPA)
- Abra o módulo **CenaflixJPA**.
- Configure `src/main/resources/META-INF/persistence.xml` (URL, usuário, senha).
- Compile e execute:
  ```bash
  mvn clean install
  mvn exec:java -Dexec.mainClass="br.com.cenaflix.cenaflixjpa.CenaflixJPA"
  ```

---

## 📁 Estrutura sugerida
```
/README.md
/LICENSE
/.gitignore
/.github/workflows/build.yml
/Cenaflix/                  # Módulo Ant (Filmes)
  src/...
  BDCenaflix.sql
/CenaflixJPA/               # Módulo Maven (Podcasts/Usuários)
  src/main/java/...
  src/main/resources/META-INF/persistence.xml
  pom.xml
```
> Mantendo os módulos em pastas separadas, a evolução do projeto fica clara para recrutadores.

---

## 🧪 CI (GitHub Actions)
Este repositório inclui um workflow que detecta e compila **Ant** (se houver `build.xml`) e/ou **Maven** (se houver `pom.xml`).  
A matriz de Java pode ser ajustada conforme necessidade.

---

## 📝 Licença
Distribuído sob a licença **MIT**. Veja `LICENSE` para detalhes.

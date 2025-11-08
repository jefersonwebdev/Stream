# 💻 StreamOn PIM VIII: Plataforma de Gestão de Conteúdo

## Visão Geral do Projeto

Este projeto foi desenvolvido como parte do Programa Integrado Multidisciplinar (PIM VIII) e consiste em uma plataforma de *streaming* modular focada na **Gestão de Conteúdo para Criadores**. A solução é dividida em três camadas principais, cobrindo o frontend mobile/desktop, o backend de API e a persistência de dados.

O objetivo principal é simular um ambiente de gestão de conteúdo semelhante ao **YouTube Studio** para criadores, e um feed de consumo de conteúdo semelhante ao **YouTube Mobile**.

-----

## 🏗️ Arquitetura do Sistema

O projeto adota uma arquitetura de três camadas, utilizando tecnologias modernas da Microsoft e nativas de Android:

### 1\. Backend (API & Dados)

  * **Tecnologia:** **ASP.NET Core Web API (C\#)**.
  * **Função:** Camada de lógica de negócios, autenticação e gerenciamento de dados.
  * **Modelos de Dados Principais (Conforme DER e Diagrama de Classes):**
      * `Criador` (Usuário gestor).
      * `Conteudo` (Vídeos, Músicas, Podcasts).
      * `Playlist` e `ItemPlaylist` (Organização de conteúdo).
  * **Persistência:** Entity Framework Core e SQL Server/SQLite.

### 2\. Frontend (Protótipos de Interface)

#### A. Protótipo do Criador (Studio)

  * **Tecnologia:** **.NET MAUI (C\#)**.
  * **Plataformas Alvo:** Windows, Android, iOS (Protótipo Desktop focado).
  * **Funcionalidades Implementadas:**
      * **Dashboard/Painel de Métricas:** Visualização de estatísticas do canal (Analytics).
      * **Conteúdo/Gestão:** Visão tabular de todos os conteúdos publicados (como o *Channel Content* do YouTube Studio).
      * **Upload de Conteúdo:** Formulário para adição de novos vídeos ou mídias.

#### B. Protótipo do Consumidor (Mobile Feed)

  * **Tecnologia:** **Android Nativo (Java e XML)**.
  * **Plataforma Alvo:** Android Mobile.
  * **Funcionalidades Implementadas:**
      * Tela inicial com **`BottomNavigationView`** e **`RecyclerView`**.
      * Layout de feed de vídeos semelhante ao YouTube, incluindo cabeçalho e filtros (Chips).

-----

## 🛠️ Tecnologias Utilizadas

  * **Linguagens:** C\# (para API e .NET MAUI) e Java (para Android Nativo).
  * **Frameworks:** ASP.NET Core 8.0, .NET MAUI.
  * **Banco de Dados:** Entity Framework Core.
  * **Design:** Google Material Design e inspiração no YouTube/YouTube Studio.
  * **Ferramentas de Desenvolvimento:** Visual Studio e Android Studio.

-----

## 🚀 Como Executar o Projeto

### 1\. Executando o Backend (API)

1.  Clone este repositório.
2.  Abra a solução da API (`StreamOn_API.sln`) no Visual Studio.
3.  Configure a string de conexão no `appsettings.json` para apontar para seu banco de dados.
4.  Execute as migrações do Entity Framework Core:
    ```bash
    dotnet ef database update
    ```
5.  Execute o projeto. O Swagger será aberto em `https://localhost:XXXX/swagger`, exibindo os *endpoints* para `Criadores`, `Conteudos` e `Playlists`.

### 2\. Executando o Frontend (Protótipo Studio .NET MAUI)

1.  Abra a solução (`StreamOn_PIM_VIII.sln`) no Visual Studio.
2.  Defina o projeto `StreamOn_PIM_VIII` como projeto de inicialização.
3.  Defina o projeto para ser executado no **Windows Machine** (ou Android Emulator).
4.  **Ajuste:** Atualize a URL da API no código do cliente para a URL do seu *backend* (`https://localhost:XXXX`).
5.  Execute o projeto.

### 3\. Executando o Frontend (Protótipo Android Nativo)

1.  Abra o projeto Android (a pasta `StreamOnPIMVIII/Android`) no **Android Studio**.
2.  Deixe o Gradle sincronizar as dependências (certifique-se de que `ConstraintLayout`, `RecyclerView` e `Material` estão no `build.gradle`).
3.  Selecione um emulador ou dispositivo.
4.  Execute a `HomeActivity` para visualizar o feed de conteúdo.

-----

## 📂 Diagramas de Referência

A estrutura de dados e relacionamentos foi baseada nos seguintes diagramas:

### Diagrama Entidade-Relacionamento (DER)

### Diagrama de Classes

-----

## ✨ Contato

Este projeto foi desenvolvido por [Seu Nome/Nome da Equipe] como requisito para o PIM VIII.

**[Seu Email ou Link do LinkedIn]**

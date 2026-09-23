<img width="1064" height="1600" alt="lista-1" src="https://github.com/user-attachments/assets/f37358e5-d471-4d12-957f-e1af38858c36" />
<img width="1104" height="1600" alt="lista-2" src="https://github.com/user-attachments/assets/81911a3f-73d8-4244-ac17-e994e8af27c5" />
# lista-mobile

1. **Descreva o que é Flutter, Dart, Widgets e a diferença para o Android.**

Flutter: é um framework de código aberto criado pelo Google para desenvolver aplicações multiplataforma, como Android, iOS, Web e Desktop, utilizando uma única base de código.

Dart: é a linguagem de programação utilizada pelo Flutter. É nela que o desenvolvedor escreve a lógica e a estrutura da aplicação.

Widgets: são os componentes que formam a interface do aplicativo no Flutter. Tudo praticamente é um widget, como textos, botões, imagens, campos de entrada e até a própria tela.

Diferença para Android: o desenvolvimento Android tradicional geralmente utiliza Kotlin ou Java e as ferramentas nativas do Android, enquanto o Flutter utiliza Dart e seus próprios Widgets, permitindo criar aplicações para diferentes plataformas a partir do mesmo código.

---

2. **Tudo no Flutter é criado com Widgets. O fluxo do desenvolvimento é orientado ao Design. Built-in Flutter Widgets são conjuntos completos de widgets. As aplicações são construídas a partir da composição de widgets prontos. Cite quais são os principais e dê exemplos.**

No Flutter, a interface é construída pela composição de Widgets, que são componentes responsáveis pela aparência e pelo comportamento da aplicação.

Os principais tipos de Widgets incluem:

MaterialApp: estrutura principal de um aplicativo baseado no Material Design.
Exemplo: define o tema e as rotas do aplicativo.
Scaffold: fornece a estrutura básica de uma tela.
Exemplo: pode conter AppBar, body e FloatingActionButton.
AppBar: cria a barra superior da aplicação.
Exemplo: título da página e botões de ação.
Text: exibe textos na tela.
Exemplo: Text("Olá, mundo!").

---

3. Todos os Widgets devem conter um método chamado build. Qual o objetivo e dê um exemplo de como usar?

O método build() é responsável por construir e retornar a interface visual de um Widget. Ele define quais elementos serão exibidos na tela e como eles serão organizados.

O método recebe um BuildContext e retorna outro Widget.

Exemplo:

class MinhaTela extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: Text("Olá, Flutter!"),
      ),
    );
  }
}

---

4. No contexto de desenvolvimento de soluções mobile com Flutter, o que são Container?

O Container é um Widget usado para organizar, dimensionar e estilizar outros Widgets no Flutter.

Exemplo:

Container(
  width: 200,
  height: 100,
  color: Colors.blue,
  child: Text("Olá, Flutter!"),
)

---

5. Qual a diferença entre aplicações nativas e híbridas? Dê exemplos.

- Aplicações nativas: são desenvolvidas especificamente para um sistema operacional, utilizando suas linguagens e ferramentas próprias. Geralmente oferecem bom desempenho e acesso aos recursos do dispositivo.

Exemplos: aplicativos Android desenvolvidos com Kotlin ou Java e aplicativos iOS desenvolvidos com Swift.

- Aplicações híbridas: são desenvolvidas com tecnologias que permitem compartilhar grande parte do código entre diferentes plataformas, como Android e iOS. Isso facilita o desenvolvimento e a manutenção.

Exemplos: aplicativos desenvolvidos com Flutter (Dart), React Native (JavaScript/TypeScript) e Ionic (HTML, CSS e JavaScript).

---

6. Um padrão de arquitetura em software é uma solução reutilizável e estruturada para problemas comuns no design de aplicações. Ajuda a organizar o código, gerenciar a lógica da aplicação e garantir que as diferentes partes do sistema interajam eficientemente. Quais são os principais padrões de arquitetura de software para apps móveis?

Os principais padrões de arquitetura de software utilizados no desenvolvimento de aplicações móveis (como Flutter, Android nativo ou iOS) são:

MVC (Model-View-Controller):

Model: Gere os dados e a lógica de negócio.   
JPG

View: Interface do utilizador (UI).   
JPG

Controller: Atua como intermediário, gerindo as interações do utilizador e atualizando o Model e a View.   
JPG

MVP (Model-View-Presenter):

Semelhante ao MVC, mas o Presenter assume o papel de intermediário direto da View. A View não conhece o Model, tornando os testes unitários mais simples.

MVVM (Model-View-ViewModel):

Bastante popular no desenvolvimento móvel (Flutter, Android/Kotlin).

ViewModel: Transforma os dados do Model para a View e gere o estado da interface através de mecanismos de data binding (ligação de dados) ou fluxos reativos (como Streams ou StateNotifier no Flutter).   
JPG

Clean Architecture (Arquitetura Limpa):

Proposta por Robert C. Martin ("Uncle Bob"), divide o projeto em camadas bem definidas e independentes: Domain (regras de negócio), Data (fontes de dados, APIs e bases de dados) e Presentation/UI (interface e gestão de estado). Promove um código altamente testável, modular e desacoplado.   
JPG
+ 1

BLoC (Business Logic Component):

Muito utilizado especificamente no ecossistema Flutter. Separa a lógica de negócio da interface gráfica através do uso de Streams (entradas via Events e saídas via States).

---

7. O que é e como é usado o Material Design e o Cupertino em Flutter?

Material Design:

O que é: É o sistema de design criado pela Google, focado num estilo visual moderno, com efeitos de sombra, profundidade, transições suaves e elementos característicos do ecossistema Android.

Como é usado: No Flutter, utiliza-se a biblioteca de componentes package:flutter/material.dart e o widget principal MaterialApp. Exemplos de componentes: Scaffold, AppBar, ElevatedButton, FloatingActionButton.

Cupertino:

O que é: É o conjunto de componentes do Flutter que implementa a linguagem de design visual e a experiência de utilização do iOS (Apple).

Como é usado: Utiliza-se a biblioteca package:flutter/cupertino.dart e o widget principal CupertinoApp. Exemplos de componentes: CupertinoNavigationBar, CupertinoButton, CupertinoTabBar, CupertinoAlertDialog.

---

8. O que é .NET MAUI? Compare com o Flutter e Android.

O que é o .NET MAUI?

O .NET MAUI (.NET Multi-platform App UI) é uma framework multiplataforma da Microsoft (evolução do Xamarin.Forms) para criar aplicações nativas para Android, iOS, macOS e Windows utilizando C# e XAML a partir de uma única base de código.

* **Comparação entre .NET MAUI, Flutter e Android:**

| Característica | .NET MAUI | Flutter | Android Nativo |
| --- | --- | --- | --- |
| **Desenvolvedor** | Microsoft | Google | Google|
| **Linguagem** | C# / XAML | Dart| Kotlin / Java |
| **Plataformas Alvo** | Android, iOS, Windows, macOS | Android, iOS, Web, Windows, macOS, Linux| Exclusivo para Android |
| **Renderização da UI** | Utiliza os **componentes nativos** de cada sistema operativo por baixo. | Desenha a sua própria UI do zero usando um motor gráfico próprio (**Skia/Impeller**).| Utiliza os componentes nativos do ecossistema Android. |
| **Desempenho** | Próximo do nativo, mas depende do mapeamento dos componentes nativos. | Excelente desempenho gráfico constante (DirectX/Metal/Vulkan).| **Desempenho máximo** em dispositivos Android por ser 100% nativo. |
| **Casos de Uso** | Recomendado para equipas com experiência no ecossistema .NET/C# ou aplicações empresariais integradas no ecossistema Microsoft. | Ideal para aplicações multiplataforma com design personalizado e idêntico em todas as plataformas.| Ideal para aplicações que necessitam de acesso profundo e exclusivo a recursos de hardware específicos do Android. |

---
 
9. Qual a diferença entre Hot Reload e Hot Restart?

Hot Reload:

O que faz: Injeta o código modificado diretamente na Máquina Virtual (VM) do Dart em execução sem reiniciar a aplicação.

Estado da app: Preserva o estado atual da aplicação (por exemplo, contadores, dados introduzidos em formulários ou navegação de ecrãs mantêm-se).

Velocidade: É extremamente rápido (geralmente leva menos de um segundo).

Uso ideal: Ajustes de interface visual (UI), pequenas alterações de estilo e correção de erros simples.

Hot Restart:

O que faz: Destrói o estado atual e reinicia completamente a aplicação, executando o método main() do zero.

Estado da app: Perde o estado atual da aplicação (volta ao ecrã/estado inicial).

Velocidade: É um pouco mais lento que o Hot Reload, mas ainda muito mais rápido do que compilar e reexecutar a aplicação do zero (Full Restart).

Uso ideal: Alterações na lógica de inicialização, modificação de initState(), alteração de variáveis globais ou quando o Hot Reload não reflete as mudanças efetuadas.

---

10. Explique o que faz o código abaixo:


O código apresentado é um ponto de entrada (*entry point*) simples de uma aplicação **Flutter**. Aqui está a explicação detalhada do que cada parte faz:

1. **`import 'package:flutter/material.dart';`** (Linha 1)


* Importa a biblioteca do Material Design do Flutter, disponibilizando os widgets visuais padrões (como `MaterialApp`, `Scaffold`, etc.).




2. **`void main() => runApp(...)`** (Linhas 3-4)


* A função `main()` é o ponto inicial de execução do programa em Dart.
* A função `runApp()` recebe o widget principal e coloca-o como raiz da árvore de widgets na tela do dispositivo.




3. **`MaterialApp(...)`** (Linha 4)


* Configura o widget raiz da aplicação com o estilo Material Design, gerindo a navegação e o tema geral.


* **`title: 'Whatsapp Clone'`** (Linha 5): Define o título da aplicação (usado pelo sistema operativo no menu de apps recentes).




4. **`home: Scaffold(...)`** (Linha 6)


* Define o ecrã inicial da aplicação utilizando o widget `Scaffold`, que fornece a estrutura básica visual de uma página (com suporte para barras de título, fundo, menus, etc.).




5. **`body: FlutterLogo(size: double.infinity)`** (Linhas 7-8)


* Define o corpo principal do ecrã (`body`).
* Exibe o widget `FlutterLogo` (o logótipo oficial do Flutter) expandido para ocupar todo o espaço disponível no ecrã (`size: double.infinity`).





---



11. O que é e qual a diferença entre Provider e Riverpod?


#### **O que são?**

Tanto o **Provider** como o **Riverpod** são bibliotecas de **gestão de estado** e **injeção de dependências** para aplicações **Flutter**, criadas pelo mesmo autor (Remi Rousselet). Servem para partilhar dados, controlar o estado da aplicação e reconfigurar a interface do utilizador (UI) quando os dados mudam.


#### **Diferenças Principais:**

1. **Dependência da Árvore de Widgets (`BuildContext`):**
* **Provider:** Depende fortemente da árvore de widgets (`BuildContext`). Para aceder a um estado, o widget precisa de estar abaixo do `Provider` correspondente na árvore.
* **Riverpod:** **Não depende de `BuildContext**`. Funciona de forma global e fora da árvore de widgets, permitindo aceder, ler ou modificar estados de qualquer lugar do código (como em controladores, serviços ou tarefas em segundo plano).


2. **Segurança de Compilação (*Compile-time Safety*):**
* **Provider:** Pode lançar erros em tempo de execução (*runtime*) caso se tente aceder a um estado que não foi declarado acima na árvore de widgets (`ProviderNotFoundException`).
* **Riverpod:** Garante segurança total em tempo de compilação. Se o código compila, o estado está acessível e disponível, eliminando erros em tempo de execução.


3. **Múltiplas Instâncias do Mesmo Tipo:**
* **Provider:** Tem dificuldade em gerir múltiplos provedores do mesmo tipo de dado dentro do mesmo escopo sem criar contornos complexos.
* **Riverpod:** Permite criar múltiplos *providers* do mesmo tipo sem qualquer tipo de conflito.


4. **Testabilidade e Desempenho:**
* **Provider:** Exige a montagem da árvore de widgets do Flutter para realizar testes unitários aos estados.
* **Riverpod:** Facilita imenso os testes unitários, permitindo testar toda a lógica de negócio de forma isolada, sem necessidade de inicializar o ambiente de widgets do Flutter.

---

12. explique o widgets tree abaixo:
<img width="1000" height="608" alt="a410b23f-3df9-460a-8db5-1d88877f97ce" src="https://github.com/user-attachments/assets/147e3b4d-11e1-4bc4-af0b-467c882da697" />

A **Widget Tree** (árvore de widgets) ilustrada na imagem representa a estrutura hierárquica e em árvore que o framework Flutter utiliza para construir e renderizar a interface de utilizador. No Flutter, **tudo é um widget**, desde os componentes estruturais até aos elementos de layout, texto e ícones.

### Estrutura e Hierarquia do Diagrama:

1. **`MyApp` e `MaterialApp**`:
* Representam a raiz da aplicação. O `MaterialApp` configura as definições globais, como temas, navegação e estilo visual no padrão Material Design.


2. **`MyHomePage` e `Scaffold**`:
* `MyHomePage` é a página/ecrã principal.
* `Scaffold` fornece a estrutura visual base de uma página típica (barra superior, corpo central, botão flutuante, etc.).


3. **Filhos do `Scaffold**`:
* **`FloatingActionButton` $\rightarrow$ `Icon**`: Cria o botão flutuante circular no canto inferior direito que contém um ícone (`Icon`).
* **`AppBar` $\rightarrow$ `Text**`: Representa a barra superior da aplicação que contém o título (`Text`).
* **`Center` $\rightarrow$ `Column` $\rightarrow$ `Text`, `Text**`:
* O `Center` alinha o seu conteúdo ao centro do ecrã.
* A `Column` organiza os seus elementos filhos na vertical.
* Os dois widgets `Text` apresentam as mensagens no centro da tela (ex.: o contador da aplicação padrão de demonstração do Flutter).

---

13. **Qual o objetivo de um emulador?**


O objetivo de um emulador (no contexto do desenvolvimento mobile) é **simular o comportamento, hardware e sistema operativo de um dispositivo físico** (como um smartphone ou tablet Android/iOS) diretamente no computador do programador.

**Principais objetivos e vantagens:**

* **Testar aplicações sem dispositivo físico:** Permite executar, testar e depurar (*debug*) a aplicação em tempo real sem necessitar de ter vários telemóveis reais ligados ao computador.
* **Simulação de múltiplos cenários:** Permite testar a aplicação em diferentes tamanhos de ecrã, resoluções, versões do sistema operativo, orientação (retrato/paisagem) e condições de rede ou bateria.
* **Agilidade no desenvolvimento:** Integra-se diretamente com o ambiente de desenvolvimento (IDE) e suporta funcionalidades como o *Hot Reload* e *Hot Restart*, acelerando a criação e ajuste de interfaces.

---

14. **De acordo com a estrutura de desenvolvimento de um código em flutter o que são main.dart e runApp()?**


* **`main.dart`:**
* **O que é:** É o ficheiro principal (ponto de entrada) de um projeto Flutter. Contém o método `main()`, que é a primeira função a ser executada quando a aplicação é iniciada.


* **`runApp()`:**
* **O que é:** É a função global do Flutter que recebe o **Widget raiz** (o widget principal da aplicação, como o `MaterialApp`) e o anexa à ecrã do dispositivo.
* **Função:** É responsável por inflar o widget fornecido, criar a árvore de widgets (*Widgets Tree*) e iniciar o ciclo de vida da interface gráfica da aplicação.

---

15. **Os widgets podem ser classificados em Stateless e Stateful, o que são e qual a diferença?**


No Flutter, os widgets representam a interface do utilizador e dividem-se principalmente em duas categorias com base na gestão do seu **estado** (dados que podem mudar durante a execução):

* **StatelessWidget (Sem Estado):**
* **O que é:** É um widget **imutável**, ou seja, a sua estrutura e as suas propriedades não se alteram depois de ser construído.
* **Quando usar:** Ideal para elementos estáticos da interface que não mudam dinamicamente em resposta a ações do utilizador (ex.: textos fixos, ícones, botões simples, avatares ou layouts estáticos).


* **StatefulWidget (Com Estado):**
* **O que é:** É um widget **mutável** que mantém um objeto de estado interno (`State`). Ele pode ser redesenhado na tela sempre que o seu estado interno for alterado através da chamada do método `setState()`.
* **Quando usar:** Necessário quando a interface precisa de reagir e atualizar os dados visíveis conforme o utilizador interage com a app (ex.: contadores, campos de texto, *checkboxes*, formulários ou listas dinâmicas).



#### **Resumo da Diferença:**

| Característica | StatelessWidget | StatefulWidget |
| --- | --- | --- |
| **Mutabilidade** | Imutável (não muda) | Mutável (pode mudar) |
| **Estado Interno** | Não possui estado alterável | Possui um objeto `State` associado |
| **Atualização na UI** | Só é reconstruído se o widget pai mudar | Reconstrói-se dinamicamente com `setState()` |
| **Desempenho** | Mais leve e rápido de renderizar | Requer um pouco mais de recursos para gerir o estado |

---

16. **O que são Scaffold e quais são?**


* **O que é o `Scaffold`?**
* É um widget fundamental do Flutter (pertencente ao pacote `MaterialApp`) que implementa a **estrutura visual básica do layout do Material Design**. Funciona como um "esqueleto" ou modelo estrutural para um ecrã, oferecendo posições pré-definidas para os elementos mais comuns da interface (como barra superior, corpo da página, botões flutuantes, etc.).


* **Quais são os principais componentes/propriedades do `Scaffold`?**

1. **`appBar`:** A barra superior da aplicação (geralmente exibe o título da página, botão de voltar e ações de menu).
2. **`body`:** O corpo principal do ecrã, onde fica o conteúdo primário (ex.: listas, formulários, imagens, colunas).
3. **`floatingActionButton`:** Um botão flutuante de ação rápida (geralmente posicionado no canto inferior direito, usado para ações principais como criar ou adicionar algo).
4. **`drawer`:** Um menu de navegação lateral deslizante (puxado do canto esquerdo da tela).
5. **`endDrawer`:** Um menu de navegação lateral deslizante a partir do canto direito.
6. **`bottomNavigationBar`:** A barra de navegação inferior (usada para alternar rapidamente entre as abas ou ecrãs principais da app).
7. **`bottomSheet`:** Um painel persistente ou modal que surge a partir da parte inferior do ecrã.
8. **`snackBar`:** Mensagens temporárias apresentadas na parte inferior do ecrã (geridas através do `ScaffoldMessenger`).

---

17. A questão 17 pede: **«Explique o que é cada componente dessa interface mobile:»**


Com base na imagem do diagrama da interface mobile apresentada no exercício, aqui está a explicação de cada um dos componentes apontados:

1. **`MaterialApp`:**
* **O que é:** É o widget raiz que envolve toda a aplicação (ou a estrutura principal). Define a identidade visual global baseada no **Material Design**, configurando o tema, as cores, as rotas de navegação e o idioma da aplicação.

2. **`Scaffold`:**
* **O que é:** É o widget estrutural que fornece o "esqueleto" visual para a ecrã da aplicação. Ele cria e organiza as áreas padrão do layout móvel, tais como a barra superior, o corpo central e a área de botões.

3. **`AppBar`:**
* **O que é:** É a barra de título localizada no topo do ecrã. Neste exemplo, contém o texto `"Simple Flutter App"` para indicar o nome ou o título da página atual.

4. **`Text`:**
* **O que é:** É o widget responsável por renderizar e exibir cadeias de caracteres (texto) no ecrã. Na imagem, é utilizado para desenhar o título dentro da `AppBar` (e pode ser usado em qualquer outra parte do layout para apresentar informação textual).

5. **`Button` (ou `ElevatedButton` / `TextButton`):**
* **O que é:** É um elemento interativo da interface do utilizador que executa uma ação ou função quando é clicado/tocado. Na imagem, surge posicionado no corpo (`body`) do ecrã com o rótulo `"Hello, Flutter!"`.


---

20. **Cite os requisitos para o desenvolvimento mobile usando flutter para o Android e para o iOS?**


#### **1. Requisitos para Android:**

* **Sistema Operativo:** Windows, macOS ou Linux.
* **Ferramentas e SDKs:**
* **Flutter SDK** instalado e configurado nas variáveis de ambiente.
* **Android Studio** (fornece a gestão do SDK do Android, *Android SDK Command-line Tools* e licenças).
* **Android SDK** (incluindo *Build-Tools* e *Platform-Tools*).
* **Java Development Kit (JDK)** (normalmente incluído no Android Studio).


* **Emulador/Dispositivo:**
* **Android Emulator** (configurado via AVD Manager no Android Studio) ou um **dispositivo físico Android** com o *Modo de Depuração USB* (*USB Debugging*) ativado.


#### **2. Requisitos para iOS:**

* **Sistema Operativo:** **macOS obrigatoriamente** (não é possível compilar ou testar apps iOS nativamente em Windows ou Linux).
* **Ferramentas e SDKs:**
* **Flutter SDK** instalado.
* **Xcode** (descarregado via Mac App Store, inclui o SDK do iOS, simuladores e ferramentas de compilação).
* **CocoaPods** (gestor de dependências para projetos iOS/macOS).


* **Emulador/Dispositivo:**
* **Simulator do iOS** (incluído com o Xcode).
* Para rodar em um **dispositivo físico Apple**: É necessária uma **Conta de Desenvolvedor Apple** (*Apple Developer Account*) configurada para assinar os certificados de desenvolvimento (*Provisioning Profiles*).

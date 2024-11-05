![](https://blog.runrun.it/wp-content/uploads/2023/12/142695-Clusterizacao-DEV-Desenvolvimento-de-software-blog-2.png)
# Programação

## Sobre
Programar (ou desenvolver um software) é o processo de criar instruções (códigos) que o computador interpreta ou executa para realizar uma tarefa ou solucionar um problema.

## Fundamentos

### Variável
Espaço em memória que armazena um valor ou referência a um objeto, acessível pelo nome dentro de seu escopo.

### Método
Método (ou Função) é bloco de código que define uma ação a ser realizada por uma classe ou objeto, podendo receber parâmetros, manipular variáveis e retornar valores.

A __Assinatura__ é a declaração do método que inclui _nome, tipo de retorno, e parâmetros_, permitindo sua identificação e uso no programa.

### Procedimento
Similar a um método, mas sem valor de retorno.

### Estruturas de Armazenamento
Mecanismos que organizam e armazenam dados de forma estruturada, com tipos como:
- __Array__: Armazena elementos em uma sequência fixa, acessados por índices.
- __Lista__: Armazena elementos de forma sequencial, permitindo adição, remoção e acesso iterativo.
- __Pilha__: Segue o princípio LIFO (Last In, First Out), com operações de inserção (push) e remoção (pop).
- __Fila__: Segue o princípio FIFO (First In, First Out), com operações de inserção e remoção.
- __Map__: Estrutura associativa que armazena pares de chave-valor.

### Estruturas de Repetição
Permitem repetir instruções enquanto uma condição é verdadeira. Tipos comuns incluem:
- __For__: Repetição de instruções por um número específico de vezes usando uma variável de controle.
- __While__: Repetição enquanto uma condição é verdadeira.
- __Do-while__: Executa pelo menos uma vez e repete enquanto a condição for verdadeira.

### Estruturas de Condição
- __If-else__: Executa um conjunto de instruções se a condição for verdadeira; outro, se falsa.
- __Case__: Seleciona entre várias ações com base no valor de uma expressão ou variável, evitando múltiplos condicionais.

## Programação Orientada a Objetos
![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*MVbw8ZiGKbuS50tw.png)

Programação Orientada a Objetos (OOP) é um paradigma de programação que utiliza Classes e Objetos para representar entidades do mundo real, encapsulando dados e comportamentos em um conjunto coeso e modular. Isso permite o reuso, a extensibilidade e a organização estruturada do código.

### Vantagens
- Confiável: O isolamento entre as partes gera um programa seguro; ao alterar uma parte, nenhuma outra é afetada.
- Oportuno: Ao dividir tudo em partes, várias podem ser desenvolvidas em paralelo.
- Manutenível: Atualizar um programa é mais fácil, e uma pequena modificação beneficia todas as partes que usam o objeto.
- Extensível: O programa não é estático e deve crescer para permanecer útil.
- Reutilizável: Objetos de um sistema podem ser usados em outros sistemas futuros.
- Natural: Facilita a compreensão, permitindo foco na funcionalidade em vez de detalhes de implementação.

### Classe
Modelo que define a estrutura e o comportamento dos objetos criados a partir dela. É considerado um dos pilares da POO, representando a Abstração.

### Objeto
Instância de uma classe que possui seus próprios valores de atributos e pode executar os métodos definidos pela classe.

### Interface
Contrato que define métodos abstratos. Características:
- Não pode ser instanciada.
- Não pode conter atributos.
- Não pode conter métodos concretos.
- Pode definir um tipo.

### Classe Abstrata
Semelhante a uma interface, mas com algumas diferenças:
- Deve conter pelo menos um método abstrato.
- Não pode ser instanciada.
- Pode conter atributos.
- Pode conter métodos concretos.
- Pode definir um tipo.

### Método Abstrato
Método sem corpo, contendo apenas a assinatura. Pode existir apenas em interfaces ou classes abstratas.

### Classe Concreta
- Não pode conter métodos abstratos.
- Pode ser instanciada.
- Pode conter atributos.
- Pode definir um tipo.

### Encapsulamento - 1° Pilar
Conceito que visa proteger os atributos e métodos concretos de uma classe, permitindo acesso apenas por meio de métodos públicos.

#### Níveis de Acesso
- Público: Acessível a qualquer classe.
- Privado: Acessível apenas à própria classe.
- Protegido: Acessível à própria classe e suas subclasses.

### Herança - 2° Pilar
Extensão de uma classe (super) através de outra classe (sub). A subclasse incorpora os métodos e atributos da superclasse, conforme o nível de acesso. A implementação de uma interface por uma classe também é considerada herança.

### Polimorfismo - 3° Pilar
Sobreposição
Conceito onde uma classe substitui o comportamento de um método herdado de sua classe pai, mantendo a mesma assinatura, alterando sua funcionalidade conforme as necessidades da classe.

### Sobrecarga
Conceito que permite a criação de vários métodos com o mesmo nome, mas com diferentes parâmetros ou tipos de retorno, possibilitando a execução da mesma operação com diferentes argumentos.

## SOLID

### Responsabilidade Única (SRP)
A mesma classe que conecta-se ao DB não deve conectar-se a um E-mail ou gerar um relatório. Cada classe, método ou objeto deve ter somente uma responsabilidade.

### Aberto/Fechado (OCP)
Crie uma interface e a implemente conforme cada necessidade.

### Substituição de Liskov (LSP)
A classe filha deve ser capaz de executar todos os métodos da classe mãe.

```Java
public class Estudante {

    public void estudar() {
        //
    }

    public void entregarTcc() {
        //
    }

}

public class EstudantePosGraduacao extends Estudante {

    @Override
    public void estudar() {
        //
    }

}
```

O exemplo acima não segue o LSP, pois por mais que um estudante de Pós-Graduação seja um estudante, ele não faz TCC.

É fácil resolver:
- A classe Estudante só deve ter o método estudar.
- Seria criada a classe `EstudanteGraduacao` para o método `entregarTcc`, e que herdaria de Estudante.
- E assim a classe `EstudantePosGraduacao` poderia herdar de Estudante.
- Ambas vão ter o método `estudar`, e criar seus métodos específicos quando necessário.

### Segregação de Interface (ISP)
Semelhante ao LSP, a classe que implementa uma interface não deve ser obrigada a implementar métodos que ela não precisa.

Toda classe criada para implementar uma interface, ela só deve existir caso seja necessário todos os métodos da interface, do contrário a interface não é apropriada para a tal classe.

### Inversão de Dependência (DIP)
Um módulo (classe, método ou entidade) não deve depender de detalhes de implementação diretamente, dDeve haver uma interface entre eles.

***O Robert C. Martin em 1996, explica que o efeito ao usar rigorosamente os Princípios do OCP and LSP, pode ser generalizado em um princípio só para ele chamado de Dependency Inversion Principle.***

```Java
public interface UserRepository {}


public class UserService {

    // Dependência
    private final UserRepository repository;

    public UserService(UserRepository repository) {
        this.repository = repository;
    }

}


// Implementações
public class JpaUserRepository implements UserRepository {}
public class JdbcUserRepository implements UserRepository{}


// Injeção de Dependência
var service = new UserService(new JpaUserRepository());
service = new UserService(new JdbcUserRepository());
```

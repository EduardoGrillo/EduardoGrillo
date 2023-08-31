# Bem-vindo ao meu perfil do GitHub!

Olá! Sou [Seu Nome], e este é o meu perfil no GitHub. Aqui você encontrará uma coleção de projetos, códigos e ideias que refletem a minha jornada de aprendizado e exploração.

## Sobre Mim

- 👩‍💻 Desenvolvedor(a) Apaixonado(a)
- 🌱 Aprendendo e crescendo todos os dias
- 🎮 Amante de jogos e tecnologia
- 📚 Compartilhando conhecimento e experiências

## Projetos em Destaque

- [Nome do Projeto 1](link_do_projeto_1) - Breve descrição do projeto.
- [Nome do Projeto 2](link_do_projeto_2) - Breve descrição do projeto.

## Joguinho em C++

### Jogo da Adivinhação

![Jogo da Adivinhação](c++_game.png)

Um simples jogo de adivinhação onde você tenta adivinhar o número gerado aleatoriamente. Teste sua intuição!

```cpp
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    srand(time(0));
    int numeroAleatorio = rand() % 100 + 1;
    
    int tentativa, tentativas = 0;
    bool acertou = false;

    cout << "Bem-vindo ao Jogo da Adivinhação!" << endl;
    cout << "Tente adivinhar o número entre 1 e 100." << endl;

    while (!acertou) {
        cout << "Digite sua tentativa: ";
        cin >> tentativa;
        tentativas++;

        if (tentativa == numeroAleatorio) {
            cout << "Parabéns! Você acertou em " << tentativas << " tentativa(s)." << endl;
            acertou = true;
        } else if (tentativa < numeroAleatorio) {
            cout << "Tente um número maior." << endl;
        } else {
            cout << "Tente um número menor." << endl;
        }
    }

    return 0;
}

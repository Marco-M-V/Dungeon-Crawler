# 🗡️ Dungeon Crawler

Um jogo de masmorra (*dungeon crawler*) feito em **C puro**, jogado inteiramente no console com gráficos em caracteres ASCII e visão *top-down*. Explore a vila, escolha sua arma, desça pelos três andares da masmorra — cada um mais perigoso — e enfrente o **Boss Final** para vencer.

---

## 👥 Desenvolvedores

- **[Marco Matheus Ribeiro da Silva Vinagre]**
- **[Rafael da Silva]**
  

>

---

## 📖 História

Sob a pacata vila de **Aldoria**, uma antiga masmorra selada por gerações voltou a despertar. Das suas profundezas, criaturas e sombras começaram a se espalhar pela superfície, ameaçando engolir tudo o que existe acima.

Você é o **último guardião** — o único capaz de descer pelos três andares amaldiçoados, enfrentar o que neles habita e confrontar o **Devorador de Almas**, o boss que comanda a escuridão. Restaurar a paz de Aldoria depende inteiramente da sua coragem.

---

## 🎮 Como Jogar

O objetivo é atravessar os **3 andares da masmorra** e **derrotar o Boss Final** no terceiro andar.

Antes de descer, fale com o **NPC da Vila** para escolher sua arma — ela acompanha você por toda a partida.

### Controles

| Tecla | Ação |
|:-----:|------|
| `w` | Move para cima (símbolo vira `^`) |
| `a` | Move para a esquerda (símbolo vira `<`) |
| `s` | Move para baixo (símbolo vira `v`) |
| `d` | Move para a direita (símbolo vira `>`) |
| `i` | Interage com o objeto à frente (NPC, porta, botão) |
| `o` | Ataca a célula/região à frente |
| `q` | Volta ao menu principal |

> Não há movimentação na diagonal.

### Regras principais

- O jogador começa com **3 vidas**.
- Pisar em um **espinho** (`#`) ou ser tocado por um **monstro** custa **1 vida** e reinicia a fase atual.
- Ao perder todas as vidas: **Game Over** e retorno ao menu.
- **Chaves** (`@`) são coletadas ao pisar nelas e usadas para abrir **portas fechadas** (`D`) com a tecla `i`.
- **Caixas** (`k`) bloqueiam a passagem, mas podem ser destruídas com ataque.
- Cada andar é concluído ao chegar na **escada** (`L`). O jogo é vencido ao derrotar o **Boss** (`Z`).

---

## 🔤 Significado dos Símbolos

| Símbolo | Significado |
|:-------:|-------------|
| `^` `v` `<` `>` | Jogador (direção para onde está olhando) |
| `*` | Parede — não atravessável |
| `#` | Espinho — mata o jogador ao pisar |
| `k` | Caixa — bloqueia, mas é destruível com ataque |
| `O` | Botão — executa uma ação ao ser pressionado |
| `D` | Porta fechada — precisa de chave |
| `@` | Chave — abre portas fechadas |
| `=` | Porta aberta — atravessável |
| `L` | Escada — leva ao próximo andar |
| `N` | NPC — escolha de arma (na Vila) |
| `X` | Monstro Tipo 1 — movimento aleatório |
| `Y` | Monstro Tipo 2 — perseguição simples |
| `Z` | Boss Final — comportamento único |

---

## ⚔️ Armas

Ao interagir com o NPC da Vila, escolha **1 entre 3 armas**. A arma define o padrão de ataque da tecla `o`:

- **Espada** — atinge uma região de **3 × 2 células** diretamente à frente.
- **Arco e Flecha** — atinge **4 células em linha reta** à frente.
- **Cajado** — atinge as **8 células adjacentes** ao jogador, em qualquer direção.

---

## 🏰 Estrutura dos Andares

| Local | Mapa | Destaque |
|-------|:----:|----------|
| **Vila** | 10×10 | NPC para escolher arma + entrada da masmorra |
| **1º Andar** | 10×10 | Tutorial: mover, usar chave/porta, destruir caixas |
| **2º Andar** | 15×15 | Espinhos, Monstro Tipo 1 e o botão (abre o caminho da escada) |
| **3º Andar** | 25×25 | Desafio final: Monstro Tipo 2 e o **Boss** |

### 👹 Comportamento do Boss

O Boss persegue o jogador e, a cada **4 turnos**, executa uma **investida**: avança **2 células** de uma vez na direção do jogador, cobrindo mais distância do que qualquer outro monstro consegue. Ele também resiste a **vários ataques** antes de ser derrotado — exigindo posicionamento e timing.

---

## 🤖 Uso de IA Generativa


> Durante o desenvolvimento, utilizamos IA generativa como ferramenta de apoio ao aprendizado, principalmente para:
> - tirar dúvidas sobre sintaxe da linguagem C e organização do código em funções;
> - revisar e validar a lógica dos mapas e da IA dos monstros.
>
> Todo o código entregue foi compreendido, revisado e testado pela equipe, e todos os integrantes são capazes de explicar cada parte da implementação.



---

## 📁 Estrutura do Repositório

```
.
├── main.c       # Código-fonte completo do jogo
└── README.md    # Este arquivo
```


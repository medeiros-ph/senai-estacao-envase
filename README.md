# Sistema de Produção de Garrafas — EV-01

Simulador didático de uma estação automatizada de produção e envase de garrafas, desenvolvido como recurso de apoio para uma aula técnica do SENAI.

## Sobre o projeto

O projeto demonstra a integração entre:

- **IHM:** interface de operação, seleção da receita e monitoramento;
- **CLP:** controle da sequência, temporizadores, estados e intertravamentos;
- **Campo:** sensores, esteira, magazines, válvula de envase e módulo Pick and Place.

A aplicação representa uma estação de produção na qual o operador seleciona a cor e o volume da garrafa. O sistema executa automaticamente as etapas de alimentação, movimentação, envase, tampagem e armazenamento.

## Objetivo didático

Demonstrar, de forma visual e acessível ao nível técnico, os seguintes conceitos de Automação Industrial:

- CLP Siemens S7-1200;
- TIA Portal;
- integração entre CLP e IHM;
- receitas de produção;
- entradas e saídas digitais;
- sensores e atuadores;
- máquina de estados;
- temporizadores;
- blocos funcionais;
- PROFINET;
- intertravamentos e diagnóstico de falhas.

## Como executar o simulador

O simulador funciona de forma **offline**, sem necessidade de instalação, servidor, banco de dados ou conexão com a internet.

### Passo a passo

1. Baixe ou clone este repositório.
2. Abra o arquivo `simulador-estacao-envase.html`.
3. Utilize o Google Chrome ou o Microsoft Edge.
4. Selecione a cor da garrafa.
5. Informe o volume de envase.
6. Clique em **Enviar pedido**.
7. Clique em **Start**.
8. Observe a execução da sequência na planta virtual.

## Sequência automatizada

O ciclo de produção é organizado em dez etapas:

1. Aguardar pedido;
2. Aguardar Start;
3. Início da produção;
4. Alimentação da garrafa;
5. Movimentação até o sensor de enchimento;
6. Enchimento conforme a receita;
7. Avanço até a estação de tampagem;
8. Tampagem com o módulo Pick and Place;
9. Armazenamento;
10. Finalização e confirmação da produção.

## Arquivos do projeto

| Arquivo | Descrição |
|---|---|
| `simulador-estacao-envase.html` | Simulador visual offline da estação EV-01 |
| `roteiro-preparacao-banca.html` | Roteiro de fala de 15 minutos e perguntas técnicas prováveis |
| `Plano de Aula Atualizado.pdf` | Plano de aula revisado para apresentação ou envio |
| `Plano de Aula Atualizado.md` | Versão editável do plano de aula |
| `Plano de Aula I.pdf` | Versão anterior do plano de aula |
| `Produto.pptx` | Material de apoio originalmente compartilhado |

## Recursos do simulador

O simulador apresenta:

- planta virtual da estação de produção;
- magazines para garrafas pretas, vermelhas e azuis;
- controle de cor e volume por meio da IHM;
- lâmpadas de estado;
- esteira de transporte;
- sensor de posição para o envase;
- sensor de posição para a tampagem;
- tanque e válvula de enchimento;
- módulo Pick and Place;
- armazenamento do produto final;
- tabela de entradas e saídas do CLP;
- log do processo;
- barra de progresso da sequência;
- parada, reset e emergência;
- mensagens de diagnóstico.

## Exemplo de receita

Para realizar uma demonstração rápida:

```text
Cor da garrafa: Vermelha
Volume de envase: 800 ml
```

Após clicar em **Enviar pedido** e **Start**, o simulador executará o ciclo completo.

## Aplicação no TIA Portal

Este simulador é um recurso visual e didático. Em uma aplicação real, a lógica poderia ser desenvolvida no **TIA Portal** para um CLP Siemens S7-1200, utilizando:

- tags de entradas e saídas;
- Data Blocks para armazenar a receita;
- blocos funcionais para cada módulo da máquina;
- temporizadores para as etapas do processo;
- comunicação entre a IHM e o CLP via PROFINET;
- intertravamentos de segurança;
- telas de operação e diagnóstico.

A simulação não substitui a validação elétrica, mecânica, pneumática e de segurança necessária em uma máquina industrial real.

## Bibliografia

ALGITTA, Alhade A.; MUSTAFA, S.; IBRAHIM, F.; ABDALRUOF, N.; ABUEEJELA, Yousef M. **Automated Packaging Machine Using PLC**. *International Journal of Innovative Science, Engineering & Technology*, v. 2, n. 5, p. 282–288, maio 2015. ISSN 2348-7968. Disponível em: [ResearchGate](https://www.researchgate.net/publication/277670326_Automated_Packaging_Machine_Using_PLC ).

FRANCHI, Claiton Moro. **Controladores lógicos programáveis: sistemas discretos**. São Paulo: Érica.

PETRUZELLA, Frank D. **Controlador lógico programável**. São Paulo: Makron Books.

SIEMENS. **SIMATIC S7-1200: documentação do sistema e manual de programação no TIA Portal**. Siemens AG.

## Autor

Projeto desenvolvido para avaliação de aula expositiva do curso Técnico em Automação Industrial do SENAI.

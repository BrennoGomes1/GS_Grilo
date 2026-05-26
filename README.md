Sistema de telemetria embarcado de alta precisão projetado para monitorar e salvaguardar variáveis críticas no interior de cápsulas espaciais. Desenvolvido como solução computacional para o Global Solution 2026 da FIAP, o projeto simula um ambiente de suporte à vida e integridade estrutural em tempo real, mitigando riscos operacionais através de automação IoT.



## Especificações da Arquitetura (Hardware)
O ecossistema foi projetado utilizando componentes de baixo consumo e alta resposta para simular o ambiente aeroespacial no simulador Tinkercad:

Unidade de Processamento: Arduino UNO (Microcontrolador ATmega328P).

Subsistema de Telemetria Térmica: Sensor de Temperatura Analógico TMP36.

Subsistema de Luminosidade Orbital: Sensor de Luz LDR (Light Dependent Resistor).

Subsistema de Integridade Estrutural: Sensor de Inclinação/Vibração SW-200D.

Interface Homem-Máquina (IHM): Display LCD 16x2 com comunicação paralela.

Módulo de Alerta Crítico: Matriz de LEDs indicadores de status e alarmes visuais.

## Vetores de Monitoramento e Funcionalidades
O firmware executa um loop de varredura contínua e assíncrona para analisar três vetores principais de sobrevivência:

1. Gestão Térmica Dinâmica
Mapeamento constante da temperatura interna da cápsula. Flutuações fora da zona segura ativam protocolos de contingência visual instantâneos para a tripulação.

2. Controle de Iluminação de Cabine
Monitoramento da incidência de luz (radiação solar direta ou falha elétrica interna), garantindo a eficiência energética e o conforto luminoso dentro do habitáculo.

3. Análise de Impacto e Vibração (G-Force)
Detecção instantânea de anomalias estruturais, micrometeoritos ou turbulência severa de reentrada através do monitoramento do sensor de vibração, disparando alarmes de criticidade máxima.

## Firmware & Stack Tecnológica
O núcleo do software foi desenvolvido em C/C++ nativo para sistemas embarcados, estruturado para priorizar performance e leitura limpa de portas analógicas/digitais.

C++
// Exemplo de escopo lógico do firmware
void loop() {
    lerSensores();
    processarDados();
    atualizarDisplayIHM();
    verificarAlertas();
}
Gerenciamento de Display: Biblioteca <LiquidCrystal.h> para controle de dados de 4 bits.

Lógica de Estados: Máquina de estados simples para determinar se a cápsula está em status SEGURO, ATENÇÃO ou EMERGÊNCIA.

## Como Executar a Simulação
Como o projeto está validado no ambiente virtual do Tinkercad, nenhum hardware físico é obrigatório para a homologação:

Acesse o circuito do projeto no Tinkercad.

Cole o código fonte presente na pasta /src do repositório no editor de código da plataforma.

Clique em Iniciar Simulação.

Interaja com os potenciômetros e sensores (TMP36, LDR e SW-200D) para simular anomalias espaciais e observar os alertas no LCD e LEDs.

## Alinhamento Global Solution
Este projeto foi concebido sob os critérios de inovação, escalabilidade e automação inteligente exigidos pela FIAP, aplicando os conceitos mais modernos de Internet das Coisas (IoT) para resolver desafios complexos de monitoramento em ambientes hostis.

Desenvolvido para fins acadêmicos e de engenharia de software – FIAP 2026.

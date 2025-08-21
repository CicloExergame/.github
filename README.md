# CicloExergame

CicloExergame é um **exergame sério distribuído** para suporte a sessões de telereabilitação usando um cicloergômetro adaptado. O sistema visa aumentar o engajamento e motivação de pacientes em reabilitação motora, especialmente em contextos remotos como pós-COVID-19, AVC e outros quadros clínicos que demandam fisioterapia.

## Visão Geral

O CicloExergame integra um jogo eletrônico estilo endless runner com um cicloergômetro modificado com sensores fisiológicos (batimentos cardíacos e saturação de oxigênio - SpO2). A pedalada do paciente controla o movimento do personagem, que deve coletar moedas enquanto evita obstáculos. O fisioterapeuta configura remotamente a sessão, acompanha parâmetros fisiológicos em tempo real, e pode jogar junto com o paciente.

Comunicação audiovisual integrada permite interação direta, fortalecendo a supervisão e o vínculo terapêutico mesmo à distância.

Ao final, relatórios detalhados com evolução da performance e dados fisiológicos ajudam no acompanhamento clínico.

## Funcionalidades

- Controle do personagem pelo paciente via pedaladas no cicloergômetro.
- Monitoramento contínuo e remoto dos sinais vitais do paciente: frequência cardíaca e SpO₂.
- Configuração dinâmica da sessão pelo fisioterapeuta (velocidade, duração, limites físicos).
- Jogo multiplayer distribuído: paciente e fisioterapeuta em ambientes distintos.
- Interação via videochamada integrada: áudio e vídeo em tempo real.
- Geração e gerenciamento sincronizado de obstáculos e itens colecionáveis.
- Personalização do avatar e interface pelo paciente.
- Suporte a diferentes posições de uso (sentado, deitado, e uso do membro superior).
- Registro dos dados da sessão com integração ao padrão FHIR para interoperabilidade e histórico clínico.

## Benefícios

- Ampliação do acesso à fisioterapia em domicílio ou locais remotos.
- Maior engajamento e adesão do paciente nas sessões.
- Monitoramento seguro e efetivo com alertas baseados nos parâmetros fisiológicos.
- Interação colaborativa entre paciente e fisioterapeuta melhora a motivação.
- Redução dos custos com equipamentos acessíveis e implementação prática.

## Arquitetura e Tecnologias

- Desenvolvido inicialmente em Unreal Engine, migração para Unity para funcionalidades avançadas.
- Middleware customizado para integração com Arduino, sensores e comunicação serial/Bluetooth.
- Comunicação em tempo real entre cliente (paciente) e servidor (sessão) via arquitetura cliente-servidor.
- Uso intensivo da API WebRTC para comunicação audiovisual e troca de dados.
- Implementação da lógica de gameplay em Blueprints (Unreal) e scripts (Unity).
- Interface intuitiva com HUDs para visualização de dados e interações.
- Integração futura com padrões de saúde via FHIR para interoperabilidade.

## Instalação

### Requisitos de Hardware

- Computador compatível com Windows 10/11 ou ambiente suportado pela engine do jogo.
- Cicloergômetro (tipo bicicleta estacionária) adaptado com:
  - Sensor de pedal (interruptor magnético).
  - Sensor de frequência cardíaca e SpO₂ (ex: MAX30100/30102).
- Dispositivo Arduino Uno ou similar para aquisição de dados.
- Interface para conexão serial ou Bluetooth.

### Requisitos de Software

- CicloExergame instalado (binário ou código-fonte compilado).
- Conexão de internet estável para sessão de telereabilitação.
- Navegador moderno ou aplicativo para videochamada integrado.

## Configuração

1. **Conectar sensores à placa Arduino** conforme esquema específico.
2. **Acoplar a placa ao cicloergômetro** para leitura dos sinais.
3. **Iniciar o CicloExergame**, selecionar a porta serial/Bluetooth correta correspondente ao Arduino.
4. **Configurar a sessão:**
   - Definir duração (minutos).
   - Ajustar limite mínimo e máximo para batimentos cardíacos e SpO₂.
   - Estipular velocidade alvo para as pedaladas.
   - Ativar/desativar geração de obstáculos e itens.
5. **Iniciar a sessão.**

## Uso

- O paciente pedala no ritmo definido, controlando o progresso do personagem no jogo.
- Comandos adicionais para movimentos laterais e rotações são feitos via teclado numérico ou joystick.
- O fisioterapeuta acompanha em tempo real os dados fisiológicos e o avanço do jogo.
- Caso deseje, o fisioterapeuta pode entrar como jogador para acompanhar a atividade.
- Comunicação por vídeo e áudio pode ser utilizada para orientar o paciente.
- Ao término, o sistema gera relatório com dados fisiológicos e performance para avaliação clínica.

## Avaliações e Estudos

- Avaliado com fisioterapeutas especialistas via método Delphi, com aprovação majoritária (>80%) da eficácia e usabilidade.
- Indicado para utilização em reabilitação motora pós Internação prolongada, doenças neurológicas, e reabilitação postural.
- Estudos indicam aumento significativo do engajamento e motivação do paciente.

## Desenvolvedores e Contribuição

Projeto desenvolvido no âmbito acadêmico pela Universidade Federal de Goiás, com contribuições de pesquisadores em Computação e Saúde.
Contribuições e feedback são bem-vindos para aprimoramento contínuo.


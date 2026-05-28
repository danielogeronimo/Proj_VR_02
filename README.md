🧠 Sobre o Projeto
Proj_VR_02 é um template para desenvolvimento de realidade virtual na Unity que expande a base inicial do Proj_VR_01. A principal inovação deste projeto é a inclusão de sistemas de animação interativos, permitindo que elementos do ambiente virtual reajam a gatilhos e ações do usuário.

✨ Funcionalidades
✅ Integração Oculus VR (suporte nativo para Oculus Quest)

✅ Universal Render Pipeline (URP) com materiais otimizados

✅ Animações funcionais com portas que se abrem ao se aproximar

✅ Modelos 3D animáveis (personagens e criaturas alienígenas)

✅ Performance adaptativa para dispositivos móveis (Adaptive Performance)

✅ Camadas de composição (Composition Layers) para interface VR

✅ Estrutura pronta para adicionar interações e locomoção

🎬 Sistema de Animação
O projeto inclui um sistema de animação funcional e expansível:

Recurso	Descrição
Animações de portas	Door Animation.anim e celeiro_door_Animation.anim para abrir/fechar portas ao se aproximar
Controladores Mecanim	Dois controladores de estado (front_door.controller e front_door 1.controller) para gerenciar as transições de animação
Personagem anime	Modelo Anime_character.fbx (com arquivo fonte .blend) para animação de personagens no mundo VR
Modelo alienígena	Asset Test_Alien-Animal-Blender_2.81.fbx para personagens não-humanos
Sistema de gatilhos	Estrutura para acionar animações baseada em colisores invisíveis – a animação é reproduzida uma única vez quando o jogador se aproxima
Como funciona a animação
As animações de porta utilizam um box collider invisível posicionado na frente da porta. Quando o jogador entra na área de detecção, um script aciona a animação correspondente, que é reproduzida integralmente. Este mesmo princípio pode ser aplicado a outros objetos interativos do cenário.

🛠️ Tecnologias Utilizadas
Unity (com suporte VR ativado)

Universal Render Pipeline (URP)

Oculus Integration SDK

Mecanim Animation System

Adaptive Performance

Composition Layers (OVR)

📁 Estrutura do Projeto
text
Proj_VR_02/
├── Assets/
│   ├── Adaptive Performance/          # Configurações de performance adaptativa
│   ├── CompositionLayers/             # Camadas de composição do Oculus
│   ├── Material/                      # Materiais do projeto
│   ├── Oculus/                        # SDK e configurações Oculus
│   ├── Plugins/                       # Plugins para Android
│   ├── animation/                     # 🎬 Sistema de animação
│   │   ├── Door Animation.anim        # Animação de abertura/fechamento de porta
│   │   ├── celeiro_door_Animation.anim # Animação para porta de celeiro
│   │   ├── front_door.controller      # Controlador Mecanim
│   │   └── front_door 1.controller    # Controlador alternativo
│   └── caracter/                      # 🎭 Modelos 3D animáveis
│       ├── anime_character/           # Personagem estilo anime (FBX + blend)
│       └── fbx_alien-animal/          # Criatura alienígena
├── Packages/                          # Manifesto e dependências
├── ProjectSettings/                   # Configurações gerais
├── UserSettings/                      # Configurações locais
└── README.md                          # Este arquivo
⚙️ Pré-requisitos
Unity 2020.3 LTS ou superior com suporte ao Universal Render Pipeline (URP)

Oculus Integration instalado via Unity Asset Store ou Package Manager

Oculus PC SDK ou Oculus Mobile SDK (dependendo da plataforma alvo)

🚀 Configuração do Ambiente
Clone o repositório:

bash
git clone https://github.com/danielogeronimo/Proj_VR_02.git
Abra o projeto na Unity:
Selecione a pasta Proj_VR_02.

Configure o suporte VR:

Edit > Project Settings > Player > Other Settings > Virtual Reality Supported (ativado)

A SDK do Oculus deve estar listada

Configure as animações (se necessário):

Os arquivos .anim e .controller já estão configurados e prontos para uso

Para visualizar o Animator Controller: Window > Animation > Animator

Configure gatilhos de animação (expansão):

Adicione um Box Collider (Is Trigger) ao redor de objetos animáveis

Crie um script simples que, ao OnTriggerEnter, chame animator.SetTrigger("Abrir")

Configure as transições no Animator Controller

Build para o dispositivo VR:

Para Oculus Quest: mude a plataforma para Android e configure as permissões necessárias

Para Oculus Rift: use a plataforma Windows, Mac ou Linux

🔧 Configurações Importantes
Configuração	Onde encontrar	Valor recomendado
Suporte VR	Project Settings > Player > XR Settings	Ativado
OpenXR	Project Settings > XR Plug-in Management	Habilitar para Windows/Android
Tracking Origin	XR Origin > Tracking Origin Mode	Floor
Animations	Configuração padrão Mecanim	Legacy ou Humanoid (dependendo do modelo)
🤝 Como Contribuir
Contribuições são bem-vindas! Para contribuir:

Faça um fork do projeto

Crie uma branch para sua feature:
git checkout -b minha-feature

Commit suas mudanças:
git commit -m 'Adiciona nova animação ou interação'

Push para a branch:
git push origin minha-feature

Abra um Pull Request no GitHub

📄 Licença
Este projeto é distribuído sob a licença MIT (consulte o arquivo LICENSE para mais informações).

📬 Contato
Autor: danielogeronimo

Repositório: https://github.com/danielogeronimo/Proj_VR_02


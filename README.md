***[💊 MedSmart](https://www.figma.com/make/MsNZkHpprtDGEdfiXkXYav/App-MedSmart-2025-Prot%C3%B3tipo-?fullscreen=1&t=UbuYOBRcTjLV03uC-1)***
O MedSmart é uma aplicação desenvolvida para atuar como um assistente inteligente na gestão de saúde, focado na simplificação de receitas médicas e na organização de cronogramas de medicação. O projeto visa proporcionar mais segurança e autonomia para pacientes com rotinas de tratamento complexas.

⚠️ **Status do Projeto: Protótipo em Desenvolvimento**
O MedSmart encontra-se atualmente em fase de prototipagem e desenvolvimento inicial. As funcionalidades descritas fazem parte da visão do produto e estão sendo implementadas.

🎯 **Objetivo**
Reduzir os riscos associados à administração incorreta de medicamentos, centralizando informações essenciais de saúde em uma única plataforma digital e auxiliando o usuário na manutenção de seus hábitos de cuidado pessoal.

🚀 **Funcionalidades Planejadas**
Gerenciamento de Medicamentos: Cadastro detalhado de remédios, incluindo dosagens e horários específicos.

- *Sistema de Alertas*: Notificações automáticas para garantir a pontualidade das doses.
- *Histórico de Adesão*: Registro das doses tomadas para acompanhamento da evolução do tratamento e monitoramento de esquecimentos.
- *Monitoramento de Sinais*: Acompanhamento de indicadores de saúde (como sinais vitais).
- *Interface Simplificada*: Design intuitivo focado na acessibilidade e facilidade de navegação.

🎨 **Design e Navegação**
O fluxo visual e a interface do usuário podem ser explorados através do protótipo interativo no Figma:

[🔗 Demonstração do Protótipo (Figma)](https://www.figma.com/make/MsNZkHpprtDGEdfiXkXYav/App-MedSmart-2025-Prot%C3%B3tipo-?fullscreen=1&t=UbuYOBRcTjLV03uC-1)

💻 **Estrutura Técnica** (Boilerplate)
Como parte do processo de desenvolvimento, abaixo está a estrutura básica da Tela Principal (Dashboard) traduzida para Python utilizando a biblioteca Flet:

import flet as ft

def main(page: ft.Page):
    # Configurações da página
    page.title = "MedSmart - Protótipo"
    page.padding = 0
    page.bgcolor = "#F5F5F5"
    page.window_width = 390  
    page.window_height = 844

    # --- Header ---
    header = ft.Container(
        content=ft.Column([
            ft.Text("Olá, Paciente", size=24, weight=ft.FontWeight.BOLD, color="white"),
            ft.Text("Sua saúde está 85% monitorada hoje.", color="#E0E0E0", size=14),
        ]),
        padding=ft.padding.only(left=30, top=60, right=30, bottom=30),
        bgcolor="#2D9CDB",
        width=float("inf"),
    )

    # --- Card de Próximo Remédio ---
    card_proximo_remedio = ft.Container(
        content=ft.Row([
            ft.Icon(name=ft.icons.MEDICAL_SERVICES, color="#2D9CDB", size=32),
            ft.Column([
                ft.Text("Próximo Medicamento", weight=ft.FontWeight.BOLD, size=16),
                ft.Text("Amoxicilina - 12:00h", size=14, color="black54"),
            ], spacing=2)
        ], alignment=ft.MainAxisAlignment.START),
        padding=20,
        bgcolor="white",
        border_radius=15,
        shadow=ft.BoxShadow(blur_radius=10, color="black12"),
    )

    # --- Grade de Atalhos ---
    grid_atalhos = ft.Row(
        controls=[
            ft.Container(
                content=ft.Column([
                    ft.Icon(name=ft.icons.CALENDAR_MONTH, color="white", size=24),
                    ft.Text("Agenda", color="white", weight=ft.FontWeight.W_500),
                ], alignment=ft.MainAxisAlignment.CENTER, horizontal_alignment=ft.CrossAxisAlignment.CENTER),
                bgcolor="#2D9CDB", expand=True, height=100, border_radius=15,
            ),
            ft.Container(
                content=ft.Column([
                    ft.Icon(name=ft.icons.PULSE_OUTLINED, color="white", size=24),
                    ft.Text("Sinais", color="white", weight=ft.FontWeight.W_500),
                ], alignment=ft.MainAxisAlignment.CENTER, horizontal_alignment=ft.CrossAxisAlignment.CENTER),
                bgcolor="#27AE60", expand=True, height=100, border_radius=15,
            ),
        ],
        spacing=20,
    )

    # --- Conteúdo Central ---
    content = ft.Container(
        content=ft.Column([
            card_proximo_remedio,
            ft.Container(height=10),
            grid_atalhos,
        ]),
        padding=20,
    )

    page.add(header, content)

if __name__ == "__main__":
    ft.app(target=main)

✒️ Autor
[Thayná Batista da Silva - GitHub (Desenvolvimento e Design)](https://github.com/thaynabds/)

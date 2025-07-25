import streamlit as st

# Eventos de exemplo para o mercado brasileiro
events = {
    "Eleições 2024 - Presidente": {
        "options": ["Candidato A", "Candidato B", "Outro"],
        "description": "Quem será o próximo presidente do Brasil?",
    },
    "Copa do Mundo 2026 - Brasil": {
        "options": ["Campeão", "Vice-Campeão", "Eliminado na fase de grupos"],
        "description": "Qual será o desempenho do Brasil na Copa do Mundo de 2026?",
    },
    "Inflação 2024 - Brasil": {
        "options": ["Acima de 5%", "Entre 3% e 5%", "Abaixo de 3%"],
        "description": "Qual será a taxa de inflação no Brasil em 2024?",
    },
}

st.title("Previsões Brasil")
st.write("Um mercado de previsão simplificado para eventos brasileiros.")

for event_name, event_data in events.items():
    st.subheader(event_name)
    st.write(event_data["description"])

    for option in event_data["options"]:
        st.write(f"- {option}")
        # Placeholder para previsão do usuário
        st.write("Sua previsão (sem funcionalidade de aposta):")
        st.radio("", ["Concordo", "Discordo"], key=f"{event_name}_{option}")

st.write("---")
st.write("Disclaimer: Este é um aplicativo de demonstração e não permite apostas reais.")

import requests

# Aquí puedes usar una API de deportes (requiere registro en algunas plataformas para obtener una clave API)
api_url = "https://www.chilevision.cl/chv-deportes/la-roja/chile-vs-ecuador-donde-verlo-en-vivo-y-gratis-partido-eliminatorias"
api_key = "TU_CLAVE_API"

response = requests.get(api_url, headers={"Authorization": f"Bearer {api_key}"})
if response.status_code == 200:
    data = response.json()
    print("Partidos y estadísticas:", data)
else:
    print("Error al obtener datos:", response.status_code)

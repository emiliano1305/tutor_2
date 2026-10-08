# Tutor de Python desde cero

Aplicación Streamlit en español para aprender Python paso a paso, pedir explicaciones, construir programas y entender errores. No consulta la web y no utiliza PDF ni documentos. Responde directamente mediante OpenAI.

## Requisito para conversar

Se requiere una clave válida de OpenAI API. En Streamlit Community Cloud, configúrala en **App settings → Secrets**:

```toml
OPENAI_API_KEY = "VALOR_SECRETO_COMPLETO_DE_LA_CLAVE"
OPENAI_MODEL = "gpt-4o-mini"
```

No subas la clave a GitHub, no la incluyas en `app.py` y no la compartas por chat. `OPENAI_API_KEY` debe ser el valor secreto completo de una clave API activa, no su nombre ni la contraseña de la cuenta. El botón **Probar conexión con OpenAI** hace una solicitud breve y confirma si la API responde, sin imprimir el secreto.

Cada pregunta al tutor usa la API configurada. No compartas el enlace públicamente sin considerar el uso que otras personas podrían hacer de la clave.

## Modos docentes

- **Empezar desde cero:** avanza de a una lección y parte de cero.
- **Explicarme un tema:** explicación sencilla y ejemplo.
- **Ayudarme a crear código:** construye y explica programas Python.
- **Entender o corregir un error:** analiza el error y propone una corrección.

La app intenta responder solo sobre programación en Python mediante las instrucciones del tutor; no es un filtro infalible. El código generado no se ejecuta automáticamente y puede contener errores.

## Ejecutar localmente

```bash
python -m venv .venv
# Windows PowerShell: .venv\\Scripts\\Activate.ps1
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
streamlit run app.py
```

## Despliegue en Streamlit Community Cloud

- Repositorio GitHub: el del proyecto.
- Rama: `main`.
- Archivo principal: `app.py`.
- Python: 3.12.
- Agrega `OPENAI_API_KEY` y `OPENAI_MODEL` en **App settings → Secrets**, nunca en GitHub.

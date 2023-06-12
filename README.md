- 👋 Hi, I’m @DanielleJesus
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
DanielleJesus/DanielleJesus is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
from PIL import Image, ImageDraw, ImageFont

# Define as configurações da imagem

width = 500

height = 500

background_color = (255, 255, 255)  # Branco

# Cria uma nova imagem

image = Image.new("RGB", (width, height), background_color)

draw = ImageDraw.Draw(image)

# Define as configurações do texto

font_size = 50

text_color = (0, 0, 0)  # Preto

text_position = (width // 2, height // 2)

text = "Dog Hause 7 Minas"

# Carrega a fonte desejada (certifique-se de ter o arquivo .ttf no mesmo diretório)

font = ImageFont.truetype("nome_da_fonte.ttf", font_size)

# Centraliza o texto na imagem

text_width, text_height = draw.textsize(text, font=font)

text_position = (text_position[0] - text_width // 2, text_position[1] - text_height // 2)

# Adiciona o texto na imagem

draw.text(text_position, text, font=font, fill=text_color)

# Salva a imagem gerada

image.save("logo_dog_hause.png")


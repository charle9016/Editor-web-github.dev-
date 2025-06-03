# Crear el contenido para el banner.md
banner_md = """\
<div align="center">

<img src="https://img.shields.io/badge/J-C%20%7C%20Charle%209016-black?style=for-the-badge&logo=github" alt="JC Badge" />

# ✨ JC | HexCharly
### Código, vibras y elegancia urbana 🔥

<img src="qr_charly.png" alt="QR Charly" width="200" />

---

**🖤 Proyecto creado por Charle 9016 & ChatGPT**

> *"Nada se borra, solo se encripta..."*

`HexCharly` es un CLI con alma de calle y cerebro cifrado.  
Oculta mensajes, protege tu código, deja firma en el ciberespacio.

</div>
"""

# Guardar archivo banner.md en el proyecto
banner_file_path = "/mnt/data/charly_hex_cli/banner.md"
with open(banner_file_path, "w") as f:
    f.write(banner_md)

# Añadir banner al zip
zip_final_path = "/mnt/data/JC_HexCharly_Repo_Final.zip"

from zipfile import ZipFile

with ZipFile(zip_final_path, "w") as zipf:
    for file_name in os.listdir("/mnt/data/charly_hex_cli"):
        full_path = os.path.join("/mnt/data/charly_hex_cli", file_name)
        zipf.write(full_path, arcname=file_name)




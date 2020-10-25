# Crear una descripción del módulo usando package.json. En caso de que se trate de otro lenguaje, usar el método correspondiente.

Para seguir con el lenguaje Python, voy a crear un módulo en este lenguaje. Para ello hay que crear un archivo `setup.py` en la carpeta del módulo cuyo contenido puede ser el siguiente:

```python
import setuptools

# Se suele usar el archivo README.md para una descripción más detallada del módulo
with open("README.md", "r") as fh:
    long_description = fh.read()

setuptools.setup(
    name="mi-modulo-en-python",
    version="0.0.1",
    author="kcobos",
    author_email="info@kcobos.es",
    description="Aquí se suele poner el típico TL;DR, vamos al grano del módulo",
    long_description=long_description, # el contenido del README.md
    long_description_content_type="text/markdown",
    url="https://github.com/kcobos/mi-modulo-en-python",
    packages=setuptools.find_packages(),
    classifiers=[
        "Programming Language :: Python :: 3",
        "License :: OSI Approved :: GPLv3 License",
        "Operating System :: OS Independent",
    ],
    python_requires='>=3.6',
)
```

En el fichero README.md se suele dar una descripción detallada del módulo, así como qué hacer para testear el módulo, ejemplos de uso o cómo contribuir o reportar fallos.

{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "3Xg_RQfnafXz",
   "metadata": {
    "id": "3Xg_RQfnafXz"
   },
   "source": [
    "# ¡Llena ese carrito!"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "mhIvmmkW414q",
   "metadata": {
    "id": "mhIvmmkW414q"
   },
   "source": [
    "# Introducción\n",
    "\n",
    "Instacart es una plataforma de entregas de comestibles donde la clientela puede registrar un pedido y hacer que se lo entreguen, similar a Uber Eats y Door Dash.\n",
    "El conjunto de datos que te hemos proporcionado tiene modificaciones del original. Redujimos el tamaño del conjunto para que tus cálculos se hicieran más rápido e introdujimos valores ausentes y duplicados. Tuvimos cuidado de conservar las distribuciones de los datos originales cuando hicimos los cambios.\n",
    "\n",
    "Debes completar tres pasos. Para cada uno de ellos, escribe una breve introducción que refleje con claridad cómo pretendes resolver cada paso, y escribe párrafos explicatorios que justifiquen tus decisiones al tiempo que avanzas en tu solución.  También escribe una conclusión que resuma tus hallazgos y elecciones.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "3MbyzpOQZ5Or",
   "metadata": {
    "id": "3MbyzpOQZ5Or"
   },
   "source": [
    "## Diccionario de datos\n",
    "\n",
    "Hay cinco tablas en el conjunto de datos, y tendrás que usarlas todas para hacer el preprocesamiento de datos y el análisis exploratorio de datos. A continuación se muestra un diccionario de datos que enumera las columnas de cada tabla y describe los datos que contienen.\n",
    "\n",
    "- `instacart_orders.csv`: cada fila corresponde a un pedido en la aplicación Instacart.\n",
    "    - `'order_id'`: número de ID que identifica de manera única cada pedido.\n",
    "    - `'user_id'`: número de ID que identifica de manera única la cuenta de cada cliente.\n",
    "    - `'order_number'`: el número de veces que este cliente ha hecho un pedido.\n",
    "    - `'order_dow'`: día de la semana en que se hizo el pedido (0 si es domingo).\n",
    "    - `'order_hour_of_day'`: hora del día en que se hizo el pedido.\n",
    "    - `'days_since_prior_order'`: número de días transcurridos desde que este cliente hizo su pedido anterior.\n",
    "- `products.csv`: cada fila corresponde a un producto único que pueden comprar los clientes.\n",
    "    - `'product_id'`: número ID que identifica de manera única cada producto.\n",
    "    - `'product_name'`: nombre del producto.\n",
    "    - `'aisle_id'`: número ID que identifica de manera única cada categoría de pasillo de víveres.\n",
    "    - `'department_id'`: número ID que identifica de manera única cada departamento de víveres.\n",
    "- `order_products.csv`: cada fila corresponde a un artículo pedido en un pedido.\n",
    "    - `'order_id'`: número de ID que identifica de manera única cada pedido.\n",
    "    - `'product_id'`: número ID que identifica de manera única cada producto.\n",
    "    - `'add_to_cart_order'`: el orden secuencial en el que se añadió cada artículo en el carrito.\n",
    "    - `'reordered'`: 0 si el cliente nunca ha pedido este producto antes, 1 si lo ha pedido.\n",
    "- `aisles.csv`\n",
    "    - `'aisle_id'`: número ID que identifica de manera única cada categoría de pasillo de víveres.\n",
    "    - `'aisle'`: nombre del pasillo.\n",
    "- `departments.csv`\n",
    "    - `'department_id'`: número ID que identifica de manera única cada departamento de víveres.\n",
    "    - `'department'`: nombre del departamento."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "n3Ha_cNSZ8lK",
   "metadata": {
    "id": "n3Ha_cNSZ8lK"
   },
   "source": [
    "# Paso 1. Descripción de los datos\n",
    "\n",
    "Lee los archivos de datos (`/datasets/instacart_orders.csv`, `/datasets/products.csv`, `/datasets/aisles.csv`, `/datasets/departments.csv` y `/datasets/order_products.csv`) con `pd.read_csv()` usando los parámetros adecuados para leer los datos correctamente. Verifica la información para cada DataFrame creado.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "OmlQPLlyaAfR",
   "metadata": {
    "id": "OmlQPLlyaAfR"
   },
   "source": [
    "## Plan de solución\n",
    "\n",

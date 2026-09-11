# 👟 Retro Kicks | Backend

API REST de **Retro Kicks**, una tienda de zapatillas retro. Provee los productos, las categorías y registra las órdenes que genera el frontend.

> ⚠️ **Proof of Concept:** proyecto con fines de demostración. **No es una tienda real** y no procesa pagos ni datos bancarios.

🖥️ **Repositorio del Frontend:** [retro-kicks-frontend](https://github.com/nicocortese/retro-kicks-frontend)

---

## 🛠️ Stack Tecnológico

* **Runtime:** [Node.js](https://nodejs.org/)
* **Framework:** [Express](https://expressjs.com/)
* **Base de datos:** [MongoDB Atlas](https://www.mongodb.com/atlas) con [Mongoose](https://mongoosejs.com/)

---

## 📡 Endpoints

| Método | Ruta | Descripción |
|---|---|---|
| GET | `/api` | Estado de la API |
| GET | `/api/products` | Lista de productos |
| GET | `/api/products/:id` | Detalle de un producto |
| POST / PUT / DELETE | `/api/products` · `/api/products/:id` | Crear, editar y borrar productos |
| GET / POST | `/api/categories` | Lista y alta de categorías |
| GET | `/api/categories/:slug` | Productos de una categoría (acepta slug o id) |
| POST | `/api/orders` | Crear una orden |

---

## 🚀 Instalación y Ejecución Local

**Requisitos:** [Node.js](https://nodejs.org/) 24 LTS (24.21 o superior) y Yarn (`npm install -g yarn`).
En Windows, versiones anteriores de Node pueden fallar al conectar con MongoDB Atlas (`querySrv ECONNREFUSED`).

1.  **Clonar e instalar:**
    ```bash
    git clone https://github.com/tiagocollado/retro-kicks-backend.git
    cd retro-kicks-backend
    yarn install
    ```

2.  **Configurar Variables de Entorno:**
    Copiar `.env.example` como `.env` y completarlo con los datos de tu cluster de Atlas (*Connect → Drivers*). `DB_USER` y `DB_PASS` son los del usuario de base de datos, no los de la cuenta de Atlas.

3.  **Iniciar el servidor:**
    ```bash
    yarn dev
    ```
    La API queda en [http://localhost:4000/api](http://localhost:4000/api).

**Datos:** los `_id` y las referencias a categorías se guardan como `ObjectId`, y `images` guarda nombres de archivo que existen en `public/assets/imgs` del frontend.

---
*Desarrollado colaborativamente para los amantes de la cultura sneaker.*

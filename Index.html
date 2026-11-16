<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Sistema de ventas — Punto de venta</title>
  <style>
    :root {
      --bg: #0f1419;
      --panel: #1a2332;
      --panel-2: #243044;
      --line: #334155;
      --text: #e8eef7;
      --muted: #94a3b8;
      --accent: #22c55e;
      --warn: #f59e0b;
      --danger: #ef4444;
      --blue: #38bdf8;
    }
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: "Segoe UI", system-ui, sans-serif;
      background: var(--bg);
      color: var(--text);
    }
    header {
      padding: 18px 24px;
      border-bottom: 1px solid var(--line);
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      flex-wrap: wrap;
    }
    header h1 { margin: 0; font-size: 1.35rem; }
    header p { margin: 4px 0 0; color: var(--muted); font-size: 0.9rem; }
    main {
      display: grid;
      grid-template-columns: 1.15fr 0.85fr;
      gap: 16px;
      padding: 16px;
    }
    @media (max-width: 960px) {
      main { grid-template-columns: 1fr; }
    }
    section {
      background: var(--panel);
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 16px;
    }
    h2 { margin: 0 0 12px; font-size: 1.05rem; }
    .row { display: flex; gap: 8px; flex-wrap: wrap; }
    input, button {
      font: inherit;
      border-radius: 10px;
      border: 1px solid var(--line);
      background: var(--panel-2);
      color: var(--text);
      padding: 10px 12px;
    }
    input { flex: 1; min-width: 110px; }
    button {
      cursor: pointer;
      background: var(--accent);
      color: #052e16;
      border: none;
      font-weight: 700;
    }
    button:hover { filter: brightness(1.08); }
    button.secondary { background: var(--panel-2); color: var(--text); border: 1px solid var(--line); }
    button.danger { background: var(--danger); color: white; }
    table { width: 100%; border-collapse: collapse; }
    th, td { text-align: left; padding: 8px 6px; border-bottom: 1px solid var(--line); vertical-align: middle; }
    th { color: var(--muted); font-weight: 600; font-size: 0.85rem; }
    .catalog {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
      gap: 10px;
      margin-top: 12px;
    }
    .card {
      background: var(--panel-2);
      border: 1px solid var(--line);
      border-radius: 12px;
      padding: 12px;
      display: flex;
      flex-direction: column;
      gap: 6px;
    }
    .card .actions { display: flex; gap: 6px; flex-wrap: wrap; margin-top: auto; }
    .card .actions button { flex: 1; padding: 8px; font-size: 0.85rem; }
    .price { color: var(--blue); font-weight: 700; }
    .totals div { display: flex; justify-content: space-between; margin: 6px 0; }
    .big { font-size: 1.4rem; color: var(--accent); font-weight: 800; }
    .change-box {
      margin-top: 12px;
      padding: 14px;
      border-radius: 12px;
      background: #052e16;
      border: 1px solid #166534;
    }
    .change-box.warn { background: #3f2a05; border-color: #92400e; }
    .muted { color: var(--muted); font-size: 0.9rem; }
    .ticket {
      margin-top: 14px;
      background: #fff;
      color: #111;
      border-radius: 10px;
      padding: 14px;
      font-family: ui-monospace, Consolas, monospace;
      font-size: 0.85rem;
      white-space: pre-wrap;
    }
    .qty { width: 70px; }
    .full { grid-column: 1 / -1; }
    .historial-item {
      background: var(--panel-2);
      border: 1px solid var(--line);
      border-radius: 10px;
      padding: 10px 12px;
      margin-bottom: 8px;
      display: flex;
      justify-content: space-between;
      gap: 10px;
      align-items: flex-start;
      flex-wrap: wrap;
    }
    .historial-item pre {
      margin: 0;
      font-family: ui-monospace, Consolas, monospace;
      font-size: 0.82rem;
      white-space: pre-wrap;
      flex: 1;
    }
    .ok { color: var(--accent); font-weight: 600; }
  </style>
</head>
<body>
  <header>
    <div>
      <h1>Punto de venta</h1>
      <p>Productos y ventas se guardan solos. El botón Nueva venta limpia el carrito para cobrar otro cliente.</p>
    </div>
    <div style="display:flex;gap:8px;align-items:center;flex-wrap:wrap">
      <span class="muted" id="estadoGuardado"></span>
      <button class="secondary" id="resetBtn" type="button">Nueva venta</button>
    </div>
  </header>

  <main>
    <section>
      <h2>Registrar productos</h2>
      <p class="muted">Al guardar, el producto queda guardado y no se pierde al cerrar.</p>
      <div class="row">
        <input id="nombre" placeholder="Nombre del producto" />
        <input id="precio" type="number" min="0" step="0.01" placeholder="Precio" />
        <input id="stock" type="number" min="0" step="1" placeholder="Stock" />
        <button id="addProduct" type="button">Guardar producto</button>
      </div>
      <div class="catalog" id="catalog"></div>
    </section>

    <section>
      <h2>Venta actual</h2>
      <table>
        <thead>
          <tr>
            <th>Producto</th>
            <th>Cant.</th>
            <th>Precio</th>
            <th>Subtotal</th>
            <th></th>
          </tr>
        </thead>
        <tbody id="cart"></tbody>
      </table>
      <p class="muted" id="empty">El carrito está vacío.</p>
      <div class="totals">
        <div><span>Total a pagar</span><span id="total">$0.00</span></div>
      </div>

      <h2 style="margin-top:18px">Cobro y cambio</h2>
      <p class="muted">Escribe el dinero que entrega el cliente. El sistema calcula el cambio.</p>
      <div class="row">
        <input id="pago" type="number" min="0" step="0.01" placeholder="Dinero que entrega el cliente" />
        <button id="cobrar" type="button">Cobrar y guardar venta</button>
      </div>
      <div class="change-box" id="resultado">
        <div>Cambio a devolver: <strong class="big" id="cambio">$0.00</strong></div>
        <div class="muted" id="mensaje">Escribe cuánto dinero recibe la caja.</div>
      </div>
      <div class="ticket" id="ticket" hidden></div>
    </section>

    <section class="full">
      <h2>Ventas guardadas</h2>
      <p class="muted">Historial persistente. Puedes eliminar una venta con el botón de cada registro.</p>
      <div id="historial"></div>
      <footer style="text-align: center; font-size: 12px; color: #888; margin-top: 24px; padding: 12px;">
  © 2026 Sistema de ventas — Almacén Salomé
</footer>
      <footer style="text-align: center; font-size: 12px; color: #888; margin-top: 24px; padding: 12px;">
  © Credor.-Julio Cesar Vargas Arias
</footer>
    </section>
  </main>

  <script>
    const CLAVE = "sistema-ventas-db-v3";
    const money = (n) => "Bs" + Number(n || 0).toFixed(2);

    function cargar() {
      const guardado = localStorage.getItem(CLAVE);
      if (guardado) {
        try {
          return JSON.parse(guardado);
        } catch (e) {}
      }
      const anterior = localStorage.getItem("sistema-ventas-db-v2");
      if (anterior) {
        try {
          const data = JSON.parse(anterior);
          localStorage.setItem(CLAVE, anterior);
          return data;
        } catch (e) {}
      }
      return {
        nextId: 5,
        nextVentaId: 1,
        productos: [
          { id: 1, nombre: "Café", precio: 25, stock: 50 },
          { id: 2, nombre: "Pan", precio: 12, stock: 40 },
          { id: 3, nombre: "Agua", precio: 15, stock: 60 },
          { id: 4, nombre: "Refresco", precio: 20, stock: 35 }
        ],
        ventas: []
      };
    }

    let db = cargar();
    let carrito = [];

    function guardar() {
      localStorage.setItem(CLAVE, JSON.stringify(db));
    }

    if (!localStorage.getItem(CLAVE)) {
      guardar();
    }

    const catalog = document.getElementById("catalog");
    const cartBody = document.getElementById("cart");
    const empty = document.getElementById("empty");
    const totalEl = document.getElementById("total");
    const cambioEl = document.getElementById("cambio");
    const mensaje = document.getElementById("mensaje");
    const resultado = document.getElementById("resultado");
    const ticket = document.getElementById("ticket");
    const historial = document.getElementById("historial");

    function total() {
      return carrito.reduce((s, i) => s + i.precio * i.cantidad, 0);
    }

    function marcarGuardado(texto) {
      const el = document.getElementById("estadoGuardado");
      el.textContent = texto;
      el.className = "ok";
      setTimeout(() => {
        el.textContent = "";
        el.className = "muted";
      }, 2500);
    }

    function nuevaVenta() {
      carrito = [];
      document.getElementById("pago").value = "";
      ticket.hidden = true;
      ticket.textContent = "";
      cambioEl.textContent = money(0);
      mensaje.textContent = "Escribe cuánto dinero recibe la caja.";
      resultado.className = "change-box";
      renderCart();
      marcarGuardado("✓ Nueva venta lista");
    }

    function renderCatalog() {
      catalog.innerHTML = "";
      if (!db.productos.length) {
        catalog.innerHTML = '<p class="muted">No hay productos. Agrega uno arriba.</p>';
      }
      db.productos.forEach((p) => {
        const card = document.createElement("div");
        card.className = "card";
        card.innerHTML =
          "<strong>" + p.nombre + "</strong>" +
          '<div class="price">' + money(p.precio) + "</div>" +
          '<div class="muted">Stock: ' + p.stock + "</div>" +
          '<div class="actions"></div>';
        const actions = card.querySelector(".actions");

        const btnAdd = document.createElement("button");
        btnAdd.type = "button";
        btnAdd.textContent = "Agregar a venta";
        btnAdd.onclick = function () { agregarAlCarrito(p.id); };

        const btnDel = document.createElement("button");
        btnDel.type = "button";
        btnDel.className = "danger";
        btnDel.textContent = "Eliminar";
        btnDel.onclick = function () { eliminarProducto(p.id); };

        actions.appendChild(btnAdd);
        actions.appendChild(btnDel);
        catalog.appendChild(card);
      });
    }

    function renderCart() {
      cartBody.innerHTML = "";
      empty.style.display = carrito.length ? "none" : "block";
      carrito.forEach(function (item, index) {
        const tr = document.createElement("tr");
        tr.innerHTML =
          "<td>" + item.nombre + "</td>" +
          '<td><input class="qty" type="number" min="0" value="' + item.cantidad + '" data-index="' + index + '" /></td>' +
          "<td>" + money(item.precio) + "</td>" +
          "<td>" + money(item.precio * item.cantidad) + "</td>" +
          '<td><button class="danger" type="button" data-del="' + index + '">Quitar</button></td>';
        cartBody.appendChild(tr);
      });
      totalEl.textContent = money(total());
      calcularCambio();
    }

    function renderHistorial() {
      historial.innerHTML = "";
      if (!db.ventas.length) {
        historial.innerHTML = '<p class="muted">Sin ventas todavía.</p>';
        return;
      }
      db.ventas.slice().reverse().forEach(function (v) {
        const lineas = v.items
          .map(function (i) { return "  " + i.nombre + " x" + i.cantidad + "  " + money(i.subtotal); })
          .join("\n");
        const box = document.createElement("div");
        box.className = "historial-item";
        const pre = document.createElement("pre");
        pre.textContent =
          "Venta #" + v.id + "  " + v.fecha + "\n" +
          lineas + "\n" +
          "TOTAL " + money(v.total) + "  PAGO " + money(v.pago) + "  CAMBIO " + money(v.cambio);
        const btn = document.createElement("button");
        btn.type = "button";
        btn.className = "danger";
        btn.textContent = "Eliminar esta venta";
        btn.onclick = function () { eliminarVenta(v.id); };
        box.appendChild(pre);
        box.appendChild(btn);
        historial.appendChild(box);
      });
    }

    function agregarAlCarrito(id) {
      const p = db.productos.find(function (x) { return x.id === id; });
      if (!p) return;
      if (p.stock < 1) {
        alert("No hay stock de este producto.");
        return;
      }
      const enCarrito = carrito.find(function (x) { return x.id === id; });
      if (enCarrito) {
        // Si ya está y sigue en 0, no suma; el usuario escribe la cantidad
        if (enCarrito.cantidad === 0) {
          renderCart();
          return;
        }
        if (enCarrito.cantidad + 1 > p.stock) {
          alert("No hay stock suficiente.");
          return;
        }
        enCarrito.cantidad += 1;
      } else {
        // Cantidad inicial 0: el usuario escribe cuántos quiere
        carrito.push({ id: p.id, nombre: p.nombre, precio: p.precio, cantidad: 0 });
      }
      renderCart();
    }

    function calcularCambio() {
      const pagoRaw = document.getElementById("pago").value;
      const pago = Number(pagoRaw);
      const debe = total();
      if (pagoRaw === "" || pagoRaw === null) {
        cambioEl.textContent = money(0);
        mensaje.textContent = "Escribe cuánto dinero recibe la caja.";
        resultado.className = "change-box";
        return null;
      }
      const cambio = pago - debe;
      if (cambio < 0) {
        cambioEl.textContent = money(Math.abs(cambio));
        mensaje.textContent = "Falta dinero. El cliente aún debe esa cantidad.";
        resultado.className = "change-box warn";
      } else {
        cambioEl.textContent = money(cambio);
        mensaje.textContent = cambio === 0
          ? "Pago exacto. No hay cambio."
          : "Entrega este cambio al cliente.";
        resultado.className = "change-box";
      }
      return cambio;
    }

    function eliminarProducto(id) {
      const p = db.productos.find(function (x) { return x.id === Number(id); });
      if (!p) {
        alert("No se encontró el producto.");
        return;
      }
      if (!confirm('¿Eliminar el producto "' + p.nombre + '"?')) return;
      db.productos = db.productos.filter(function (x) { return x.id !== Number(id); });
      carrito = carrito.filter(function (x) { return x.id !== Number(id); });
      guardar();
      renderCatalog();
      renderCart();
      marcarGuardado("✓ Producto eliminado");
    }

    function eliminarVenta(id) {
      const v = db.ventas.find(function (x) { return x.id === Number(id); });
      if (!v) {
        alert("No se encontró la venta.");
        return;
      }
      if (!confirm("¿Eliminar la venta #" + v.id + "?")) return;
      db.ventas = db.ventas.filter(function (x) { return x.id !== Number(id); });
      guardar();
      renderHistorial();
      marcarGuardado("✓ Venta eliminada");
    }

    document.getElementById("addProduct").onclick = function () {
      const nombre = document.getElementById("nombre").value.trim();
      const precio = Number(document.getElementById("precio").value);
      const stock = Number(document.getElementById("stock").value || 0);
      if (!nombre || !(precio > 0)) {
        alert("Escribe nombre y un precio mayor a 0.");
        return;
      }
      db.productos.push({
        id: db.nextId++,
        nombre: nombre,
        precio: precio,
        stock: Number.isFinite(stock) ? Math.max(0, stock) : 0
      });
      guardar();
      document.getElementById("nombre").value = "";
      document.getElementById("precio").value = "";
      document.getElementById("stock").value = "";
      renderCatalog();
      marcarGuardado("✓ Producto guardado");
    };

    document.getElementById("cobrar").onclick = function () {
      const itemsValidos = carrito.filter(function (i) { return i.cantidad > 0; });
      if (!itemsValidos.length) {
        alert("El carrito está vacío o las cantidades están en 0. Escribe la cantidad.");
        return;
      }
      const cambio = calcularCambio();
      if (cambio === null) {
        alert("Escribe el dinero que entrega el cliente.");
        return;
      }
      if (cambio < 0) {
        alert("Falta dinero. No se puede cobrar todavía.");
        return;
      }
      const pago = Number(document.getElementById("pago").value);
      for (let k = 0; k < itemsValidos.length; k++) {
        const i = itemsValidos[k];
        const p = db.productos.find(function (x) { return x.id === i.id; });
        if (!p || p.stock < i.cantidad) {
          alert("Stock insuficiente de " + i.nombre + ".");
          return;
        }
      }
      const items = itemsValidos.map(function (i) {
        return {
          nombre: i.nombre,
          cantidad: i.cantidad,
          subtotal: i.precio * i.cantidad
        };
      });
      itemsValidos.forEach(function (i) {
        const p = db.productos.find(function (x) { return x.id === i.id; });
        p.stock -= i.cantidad;
      });
      if (!db.nextVentaId) db.nextVentaId = 1;
      const ventaTotal = items.reduce(function (s, i) { return s + i.subtotal; }, 0);
      const venta = {
        id: db.nextVentaId++,
        fecha: new Date().toLocaleString(),
        items: items,
        total: ventaTotal,
        pago: pago,
        cambio: pago - ventaTotal
      };
      db.ventas.push(venta);
      guardar();
      ticket.hidden = false;
      ticket.textContent =
        "TICKET DE VENTA #" + venta.id + "\n" +
        "------------------------------\n" +
        items.map(function (i) { return i.nombre + " x" + i.cantidad + "  " + money(i.subtotal); }).join("\n") + "\n" +
        "------------------------------\n" +
        "TOTAL:   " + money(venta.total) + "\n" +
        "PAGO:    " + money(pago) + "\n" +
        "CAMBIO:  " + money(venta.cambio) + "\n";
      carrito = [];
      document.getElementById("pago").value = "";
      renderCatalog();
      renderCart();
      renderHistorial();
      marcarGuardado("✓ Venta guardada");
    };

    document.getElementById("pago").addEventListener("input", calcularCambio);

    cartBody.addEventListener("input", function (e) {
      if (!e.target.classList.contains("qty")) return;
      const index = Number(e.target.dataset.index);
      const item = carrito[index];
      if (!item) return;
      const p = db.productos.find(function (x) { return x.id === item.id; });
      const max = p ? p.stock : 0;
      let val = Number(e.target.value);
      if (!Number.isFinite(val) || val < 0) val = 0;
      if (val > max) val = max;
      item.cantidad = val;
      e.target.value = val;
      // actualizar solo subtotal de la fila y total
      const fila = e.target.closest("tr");
      if (fila && fila.cells[3]) {
        fila.cells[3].textContent = money(item.precio * item.cantidad);
      }
      totalEl.textContent = money(total());
      calcularCambio();
    });

    cartBody.addEventListener("click", function (e) {
      if (!e.target.dataset.del) return;
      carrito.splice(Number(e.target.dataset.del), 1);
      renderCart();
    });

    document.getElementById("resetBtn").onclick = nuevaVenta;

    renderCatalog();
    renderCart();
    renderHistorial();
  </script>
</body>
</html>

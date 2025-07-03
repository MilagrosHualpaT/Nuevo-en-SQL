# Gestión Operativa y Financiera del Banco EurekaBank
📌 Contexto:
EurekaBank ha implementado un sistema bancario que registra las operaciones financieras, cuentas, clientes, empleados y sucursales. Actualmente, se busca aprovechar estos datos para obtener inteligencia de negocio que permita:

Evaluar la eficiencia operativa.

Analizar el comportamiento del cliente.

Optimizar recursos por sucursal.

Controlar el uso de productos y servicios financieros.

🎯 Objetivos del Sistema:
Controlar los movimientos financieros por tipo (depósitos, retiros, transferencias).

Medir la productividad de los empleados (cuentas creadas, movimientos registrados).

Analizar el uso de servicios por moneda, ciudad, sucursal y cliente.

Detectar eventos críticos, como saldos negativos o cuentas canceladas.

Comparar el desempeño por periodo, ciudad y tipo de producto financiero.

Evaluar el costo y rentabilidad de operaciones según la moneda y tipo de transacción.

📦 Entidades clave (basadas en la base de datos actual):
Sucursal

chr_sucucodigo, vch_sucunombre, vch_sucuciudad, vch_sucudireccion, int_sucucontcuenta

Cliente

chr_cliecodigo, vch_cliepaterno, vch_cliematerno, vch_clienombre, chr_cliedni, vch_clieciudad, vch_cliedireccion, vch_clietelefono, vch_clieemail

Empleado

chr_emplcodigo, vch_emplpaterno, vch_emplmaterno, vch_emplnombre, vch_emplusuario, vch_emplclave

Cuenta

chr_cuencodigo, chr_cliecodigo (FK), chr_emplcreacuenta (FK), chr_sucucodigo (FK), chr_monecodigo (FK), dec_cuensaldo, dtt_cuenfechacreacion, vch_cuenestado

Movimiento

chr_cuencodigo (FK), int_movinumero, dtt_movifecha, chr_emplcodigo (FK), chr_tipocodigo (FK), dec_moviimporte, chr_cuenreferencia

Moneda

chr_monecodigo, vch_monedescripcion

TipoMovimiento

chr_tipocodigo, vch_tipodescripcion, vch_tipoaccion, vch_tipoestado

Parametro / InteresMensual / CostoMovimiento

Para reglas sobre cargos y condiciones operativas.

📘 Reglas de negocio relevantes:
Las cuentas están asociadas a un cliente, un empleado, una sucursal y una moneda.

Los movimientos están clasificados por tipo: depósito, retiro, transferencia, etc.

Si una cuenta tiene más de 15 movimientos, se cobra un cargo.

Cada moneda tiene una tasa de interés mensual asociada.

Cada moneda también tiene un costo por operación.

Cada empleado puede estar activo en una sola sucursal a la vez.

![DIAGRAMA E-R_Deysi Milagros Hualpa Ticona](https://github.com/user-attachments/assets/312c738d-94d9-4b12-883c-ec6f388be374)
![DIAGRAMA LOGICO_Deysi Milagros Hualpa Ticona](https://github.com/user-attachments/assets/0800fff5-a35a-4567-bab2-bec0eaccd1ec)
![DIAGRAMA FISICO_Deysi Milagros Hualpa Ticona](https://github.com/user-attachments/assets/84ef643f-fceb-4fc9-b4f2-144ba01da03e)




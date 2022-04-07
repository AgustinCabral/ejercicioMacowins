# ejercicioMacowins
Ejercicio Macowins para diseño de sistemas

1) Requerimientos:
Tener una interfaz para cada prenda de la empresa (donde se tendrá su precio de venta, su estado y tipo), y un método que obtenga correctamente el valor de cada una de estas. Así como tener una interfaz para cada venta realizada por la empresa. Por ultimo generar una interfaz para la empresa en si que pueda calcular la ganancia total por dia

2) Diagrama de clase y pseudocódigo:

Clase Prenda(): 
  var estado :: string
  var precioVenta :: int
  var tipoPrenda :: string

  method calculoPrecio():
    if self.estado == "Promocion":
      precioVenta = aplicarPromocion(self.precioVenta, valor)
    elif self.estado == "Liquidacion":
      precioVenta = precioVenta * 0.5
      
  
 Clase Venta():
  var prendasVendidas :: [Prenda]
  var cantidad :: Int
  var fecha :: Int 
  var metodoDePago :: string
  var costoTotal :: int 
  
  method calculoCostoTotal(coeficiente, cantidadCUotas):
    var recargo :: int
    for prenda in prendasVendida: 
      recargo += prenda.PrecioVenta * 0.01
    recargo += cantidadCuotas * coeficiente
    costoTotal += self.precioTotal() + recargo
    
   method precioTotal(): 
    var total :: int
    for prenda in prendasVendidas: 
      total += prenda.precioVenta
      
   class Macowins():
    var ventas :: [Venta]
    var prendas :: [Prenda]
    
    method ganancia(dia):
      var gananciaTotal :: int
      for venta in ventas:
       if venta.fecha == dia: 
       gananciaTotal += costoTotal
      return gananciaTotal
      

![image](https://user-images.githubusercontent.com/49699260/162332094-5b28302f-6146-4017-8e1f-15d8557257f4.png)

  
  
      

# RecoilJS

Created by: Kenny Eduard Vercaemer González
Last edited by: Alejandro Mtz. Luna
Tags: Technology, Todo
URL: https://recoiljs.org/docs/introduction/installation

# ¿Qué es RecoilJS?

Recoil es una biblioteca de administración de estado de React que hace que el manejo del estado de la aplicación sea más fácil y escalable. A continucación se presenta una pequeña guía básica para comenzar a usar Recoil en nuestra aplicación de React:

# **Instalar Recoil**

Para comenzar a usar Recoil, primero debemos de instalarlo en nuestro proyecto. Podmeos hacerlo ejecutando el siguiente comando en la terminal:

```less
npm install recoil
```

# **Configurar un átomo**

Un átomo es la unidad básica de estado en Recoil. Un átomo representa una sola pieza de estado de nuestra aplicación. Para configurar un átomo, usamos la función **`atom`** de Recoil. 

Por ejemplo:

```jsx
import { atom } from 'recoil';

export const counterState = atom({
  key: 'counterState',
  default: 0,
});
```

En este ejemplo, estamos creando un átomo llamado **`counterState`** que tiene un valor predeterminado de **`0`**. También hemos proporcionado una clave única para identificar este átomo.

# **Acceder al estado del átomo**

Para acceder al estado de un átomo, usamos el componente **`useRecoilValue`** de Recoil. Aquí hay un ejemplo:

```jsx
import { useRecoilValue } from 'recoil';
import { counterState } from './atoms';

function CounterDisplay() {
  const count = useRecoilValue(counterState);

  return <div>{count}</div>;
}
```

En este ejemplo, estamos usando **`useRecoilValue`** para obtener el valor actual del átomo **`counterState`**. Luego, mostramos el valor en un componente de visualización.

# **Actualizar el estado del átomo**

Para actualizar el estado de un átomo, usamos la función **`useSetRecoilState`** de Recoil. Aquí hay un ejemplo:

```jsx
import { useSetRecoilState } from 'recoil';
import { counterState } from './atoms';

function CounterButton() {
  const setCount = useSetRecoilState(counterState);

  const handleClick = () => {
    setCount((count) => count + 1);
  };

  return <button onClick={handleClick}>Increment</button>;
}
```

En este ejemplo, estamos usando **`useSetRecoilState`** para obtener una función **`setCount`** que podemos usar para actualizar el valor del átomo **`counterState`**. Luego, usamos esta función dentro de un controlador de clics para actualizar el valor del átomo.

Con estos cuatro pasos básicos, podemos comenzar a usar Recoil en una aplicación React. Existen muchas otras funciones y conceptos avanzados en Recoil que se pueden explorar, como los selectores y los efectos secundarios. 

# Recomendaciones para el uso de RecoilJs

---

# Documentación y recursos

<aside>
📆 Documentación oficial RecoilJS

</aside>

[Installation | Recoil](https://recoiljs.org/docs/introduction/installation)
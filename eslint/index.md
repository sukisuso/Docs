
### Configuración de eslint

1) Instalar el paquete https://www.npmjs.com/package/eslint-config-airbnb:
```
export PKG=eslint-config-airbnb;
npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG@latest"
```

2) Crearos un fichero .eslintrc a nivel global (en vuestra home) o en cada proyecto con el siguiente contenido:
```json
{
  "extends": "airbnb",
  "rules": {
    "no-plusplus": ["error", { "allowForLoopAfterthoughts": true }],
    "no-param-reassign": ["error", { "props": false }],
    "no-underscore-dangle": ["error", { "allow": ["_id"] }]
  }
}
```
La parte importante es el extends: airbnb. Si queréis reglas propias os las metéis en la propiedad rules.

3.) Instalar eslint globalmente: npm install -g eslint

4.) En el editor que uséis (atom, code, sublime, y demás mierdas, os recomiendo vim ;) ) instaláis el plugin correspondiente de eslint.

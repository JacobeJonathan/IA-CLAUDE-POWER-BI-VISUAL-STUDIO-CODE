# IA-CLAUDE-POWER-BI-VISUAL-STUDIO-CODE
Analisis Data con IA
- Nota: Desactivar proteccion de windows, desacivar antivirus, instalar todo como administrador
🎯 GUÍA RÁPIDA - CONNECT IA TO POWER BI
Guarda esto en tu Drive y comparte el link. Cualquiera puede seguirlo sin ayuda.
________________________________________
📋 CHECKLIST VISUAL (imprimir o guardar como PDF)
________________________________________
✅ PASO 1: DESCARGAS (2 minutos)
1.	Visual Studio Code → https://code.visualstudio.com/download
2.	Claude Desktop → https://claude.com/download
________________________________________
✅ PASO 2: INSTALAR EXTENSIONES EN VS CODE
Abre VS Code → Clic en Extensiones (4 cuadrados) → Busca e instala:
•	✅ Power BI Modeling MCP Server (de Microsoft)
•	✅ GitHub Copilot Chat (opcional, solo si usarás ChatGPT)
________________________________________
✅ PASO 3: OBTENER LA RUTA DEL PROGRAMA
Atajo mágico: Presiona Windows + R → pega esto → Enter
%USERPROFILE%\.vscode\extensions
Dentro de esa carpeta:
•	Busca carpeta que empieza con powerbi-mcp
•	Entra → server → bin
•	Clic derecho en powerbi-modeling-mcp.exe → "Copiar como ruta"
Guarda esa ruta en el Bloc de notas.
________________________________________
✅ PASO 4: CONFIGURAR CLAUDE
1.	Abre Claude Desktop
2.	Arriba derecha → Settings → Developer → Edit Config
3.	Borra todo y pega este código:
JSON
Copy
{
  "mcpServers": {
    "powerbi-modeling-mcp": {
      "command": "PON_AQUI_TU_RUTA",
      "args": ["--start"],
      "type": "stdio"
    }
  }
}
4.	Selecciona PON_AQUI_TU_RUTA → Bórralo → Pega la ruta que copiaste
5.	Cambia TODAS las barras \ por dobles \\ (Ctrl+H → buscar \ → reemplazar \\)
Ejemplo final:
JSON
Copy
"command": "C:\\Users\\TuUsuario\\.vscode\\extensions\\...\\powerbi-modeling-mcp.exe",
6.	Guarda: Ctrl + S → Cierra el Bloc de notas
________________________________________
✅ PASO 5: REINICIAR Y VERIFICAR
1.	Cierra Claude completamente (X, no minimizar)
2.	Reinicia tu PC (obligatorio)
3.	Abre Claude → Settings → Developer
4.	Debe decir: powerbi-modeling-mcp: Running ✅
________________________________________
✅ PASO 6: PROBAR CON POWER BI
1.	Abre Power BI Desktop (cualquier archivo)
2.	En Claude escribe:
Conéctate al archivo de Power BI Desktop abierto
3.	Luego prueba:
Crea una medida de ventas totales
4.	Clic en "Allow" → En Power BI, Refresh en Tablas → Verás la medida creada
________________________________________
**🔥 ** REGLA DE ORO **
** "Allow" = Sí, hazlo esta vez**
"Always Allow" = Sí, hazlo siempre sin preguntarme
________________________________________
📌 NOTAS RÁPIDAS
•	**¿Error "Server disconnected"? ** → Cambia --stdio por --start
•	** ¿Error "Access Denied"? ** → Ejecuta VS Code como Administrador (clic derecho → Ejecutar como administrador)
•	** ¿No funciona después de reiniciar? ** → Revisa que las barras sean dobles \\ en TODAS partes



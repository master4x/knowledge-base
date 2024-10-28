Ein **Uniform Resource Identifier (URI)** ist eine Zeichenkette, die verwendet wird, um eine Ressource im Internet eindeutig zu identifizieren. URIs ermöglichen es, Ressourcen aufzufinden, sie voneinander zu unterscheiden und auf sie zuzugreifen. Sie bilden die Grundlage für das Web, da sie den Zugriff auf Webseiten, Dateien, APIs und andere Online-Ressourcen ermöglichen.

# URI, URL und URN

Der Begriff **URI** ist eine Oberkategorie, unter die verschiedene Arten von Identifikatoren fallen. Die beiden bekanntesten Typen sind **URL** und **URN**:
- **URL (Uniform Resource Locator)**: Eine **URL** beschreibt nicht nur die Identität einer Ressource, sondern auch ihren Standort und Zugriffspfad, z. B. `https://example.com/page`.
- **URN (Uniform Resource Name)**: Eine **URN** identifiziert eine Ressource über einen dauerhaften, ortsunabhängigen Namen, ohne den tatsächlichen Zugriffspfad anzugeben, z. B. `urn:isbn:0451450523` für die ISBN eines Buches.

## Aufbau eines URI

Ein URI besteht aus mehreren Komponenten, die je nach Typ variieren können. Ein typischer URI enthält:

1. **Schema**: Der Typ des Zugriffsprotokolls, z. B. `http`, `https`, `ftp`, `mailto`.
2. **Autorität** (optional): Informationen zur Domäne, wie `example.com`.
3. **Pfad**: Der spezifische Ort der Ressource auf dem Server.
4. **Query-Parameter** (optional): Parameter, die zusätzliche Informationen übergeben, z. B. `?id=123`.
5. **Fragment** (optional): Ein Verweis auf eine Stelle innerhalb der Ressource, z. B. `#section`.

Beispiel eines vollständigen URI:
`https://example.com/path/to/resource?id=123#section`

### URI-Komponenten im Beispiel

- **Schema**: `https`
- **Autorität**: `example.com`
- **Pfad**: `/path/to/resource`
- **Query-Parameter**: `id=123`
- **Fragment**: `#section`

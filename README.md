# _**somePython**_
_**WorkingXML,Files,FileSystem,SYSModule,Practice**_

## _1.Extrayendo texto desde un documento XML_
```xml
  <!--En esta ocasion vamos a extraer Texto Plano desde un Archivo XML-->
  <!--Documento XML-->
  <?xml version="1.0" encoding="UTF-8" ?>
  <person>
    <firstname>Rebcesp</firstname>
    <lastname>Rebeca</lastname>
    <city>Bora Bora</city>
    
    <skill name="Python"/>
    <skill name="SQL"/>
    <skill name="Java"/>
    <skill name="Cloud"/>
  </person>
```

```python
  #!/usr/bin/env python
  #Trabajaremos con el XML 
  import xml.dom.minidom #Vamos a trabajar con el DOM , frecuentemente empiezan con el documento XML
  
  
  def main()
    doc=xml.dom.minidom.parse("sample.xml");
    
    print(doc.nodeName)
    print(doc.firstChild.tagName)
    
    skills = doc.getElementByTagName("skill")
    print(" %d skills: " %skills.length)
    
    for skill in skills:
      print(skill.getAttribute("name"))
      
    newSkill = doc.createElement("skill")
    newSkill.setAttribute("name","javascript")
    doc.firstChild.appendChild(newSkill)
    
    skills = doc.getElementByTagName("skill")
    print("%d skills: " % skills.length)
    
    for skill in skills:
      print(skill.getAttribute("name"))
  main()
```
  




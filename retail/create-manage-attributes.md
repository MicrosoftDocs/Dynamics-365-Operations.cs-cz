---
title: "Vytvoření a správa atributů"
description: "Tento článek popisuje atributy v 365 Microsoft Dynamics pro operace. Atributy umožňují popis produktu a jeho charakteristik prostřednictvím uživatelem definovaných polí."
author: josaw1
manager: AnnBe
ms.date: 2015-12-04 02 - 16 - 20
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>Vytvoření a správa atributů

Tento článek popisuje atributy v 365 Microsoft Dynamics pro operace. Atributy umožňují popis produktu a jeho charakteristik prostřednictvím uživatelem definovaných polí.

Atributy umožňují popis produktu a jeho charakteristik prostřednictvím uživatelem definovaných polí. Například lze zadat velikost paměti produktu a kapacitu pevného disku a uvést, zda je produkt kompatibilní se standardem Energy Star. Atributy lze přidružit k různým maloobchodním entitám, jako jsou kategorie produktů a maloobchodní sítě, a lze jim nastavit výchozí hodnoty. Produkty dědí atributy a výchozí hodnoty pro tyto atributy při přidružení ke kategorii produktu nebo maloobchodní síti. Výchozí hodnoty lze přepsat na úrovni jednotlivých produktů na úrovni maloobchodní sítě nebo v maloobchodním katalogu.

#### <a name="examples"></a>Příklad

Kategorie

Atribut

Přípustné hodnoty

Výchozí hodnota

Televize a video

Značka

Libovolná platná hodnota **Značka**

Žádné

TELEVIZE

Velikost obrazovky

**20"**–**80"**

Žádné

Svislé rozlišení

**480i**, **720p**, **1080i** nebo **1080p**

**1080p**

Obnovovací frekvence obrazovky

**60 Hz**, **120 Hz** nebo **240 Hz**

**60 Hz**

Vstupy HDMI

**0**–**10**

**3**

Vstupy DVI

**0**–**10**

**1**

Kompozitní vstupy

**0**–**10**

**2**

Komponentní vstupy

**0**–**10**

**1**

LCD

Připraveno na 3D

**Ano** nebo **Ne**

**Ano**

3D k dispozici

**Ano** nebo **Ne**

**Ne**

Plazma

Provozní teplota od

**0**–**43** °C

**32**

Provozní teplota do

**0**–**43** °C

**100**

Projekční

Záruka

**6**, **12** nebo **18** měsíců

**12**

\#Projekce trubek

**1**–**5**

**3**

## <a name="attribute-type"></a>Typ atributu
  [![atributy pevné kopie](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) atributy jsou založeny na typy atributů. Typy atributů určují typ dat, který lze zadat pro určitý atribut. V současné době 365 Microsoft Dynamics pro operace podporuje následující typy atributů:

-   **Měna** – tento typ atributu podporuje měnové hodnoty. Mohou být vázané (může tedy podporovat rozsah hodnot), nebo mohou být otevřené.
-   **Datum a čas** – tento typ atributu podporuje hodnoty data a času. Mohou být vázané (může tedy podporovat rozsah hodnot), nebo mohou být otevřené.
-   **Desetinné číslo** – tento typ atributu podporuje číselné hodnoty, které obsahují desetinná místa. Podporuje také měrné jednotky. Mohou být vázané (může tedy podporovat rozsah hodnot), nebo mohou být otevřené.
-   **Celé číslo** – tento typ atributu podporuje číselné hodnoty. Podporuje také měrné jednotky. Mohou být vázané (může tedy podporovat rozsah hodnot), nebo mohou být otevřené.
-   **Text** – tento typ atributu podporuje textové hodnoty. Podporuje také předdefinovanou sadu možných hodnot (výčtů).
-   **Logická** – tento typ atribut podporuje binární hodnoty (**true**/**false**).
-   **Odkaz**.

## <a name="attribute"></a>Atribut
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) kromě název, popisný název, popis a text nápovědy, jeden nebo více z následujících typů informací lze zachytit atributu:

-   Výchozí hodnota
-   Metadata atributu, jako jsou například metadata, která určují, zda lze atributu vyhledávat, upřesňovat a řadit

## <a name="attribute-group"></a>Skupina atributů
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) poté, co byly definovány atributy mohou být seskupeny do skupiny atributů. Skupiny atributů poskytují seskupení jednotlivých atributů a mohou být přiřazeny kategoriím maloobchodu nebo maloobchodním sítím.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Přiřazení skupin atributů ke kategoriím maloobchodu
  [![createandmanageattribute 12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) jednu nebo více skupin atributů lze přiřadit kategorie uzly v hierarchii kategorií produktů maloobchodu. Po zařazení produktů do kategorií, zdědí produkty atributy, které jsou zahrnuty ve skupinách atributů.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Přiřazení skupin atributů k maloobchodním prodejnám
  [![createandmanageattribute-13-1024 x 576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) jednu nebo více skupin atributů mohou být přidruženy k jedné nebo více maloobchodních prodejen v hierarchii maloobchodní obchody. Po upravení produktů pro konkrétní maloobchodní prodejny, zdědí produkty atributy, které jsou zahrnuty ve skupinách atributů.

## <a name="overriding-attribute-values"></a>Přepsání hodnot atributů
### <a name="at-the-product-level"></a>Na úrovni produktu

  [![createandmanageattribute-14-1024 x 576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) lze přepsat výchozí hodnoty atributů na úrovni produktu (který je pro jednotlivé produkty).

### <a name="in-a-retail-catalog"></a>V maloobchodním katalogu

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) výchozí hodnoty atributů mohou být potlačeny pro jednotlivé produkty v konkrétní katalogy, které jsou určené pro konkrétní maloobchodní sítě.

### <a name="at-the-retail-channel-level"></a>Na úrovni maloobchodní sítě

  [![createandmanageattribute 1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) výchozí hodnoty atributů mohou být potlačeny pro jednotlivé produkty v konkrétní katalogy, které jsou určené pro konkrétní maloobchodní sítě.



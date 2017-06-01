---
title: "Vytvoření a správa atributů"
description: "Tento článek popisuje atributy v aplikaci Microsoft Dynamics 365 for Operations. Atributy umožňují popis produktu a jeho charakteristik prostřednictvím uživatelem definovaných polí."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: eaee0edb4822a386c8781d9929999cea326f0a40
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="create-and-manage-attributes"></a>Vytvoření a správa atributů

[!include[banner](includes/banner.md)]


Tento článek popisuje atributy v aplikaci Microsoft Dynamics 365 for Operations. Atributy umožňují popis produktu a jeho charakteristik prostřednictvím uživatelem definovaných polí.

Atributy umožňují popis produktu a jeho charakteristik prostřednictvím uživatelem definovaných polí. Například lze zadat velikost paměti produktu a kapacitu pevného disku a uvést, zda je produkt kompatibilní se standardem Energy Star. Atributy lze přidružit k různým maloobchodním entitám, jako jsou kategorie produktů a maloobchodní sítě, a lze jim nastavit výchozí hodnoty. Produkty dědí atributy a výchozí hodnoty pro tyto atributy při přidružení ke kategorii produktu nebo maloobchodní síti. Výchozí hodnoty lze přepsat na úrovni jednotlivých produktů na úrovni maloobchodní sítě nebo v maloobchodním katalogu.

#### <a name="examples"></a>Příklad

| Kategorie   | Atribut                | Přípustné hodnoty          | Výchozí hodnota |
|------------|--------------------------|-----------------------------|---------------|
| Televize a video | Značka                    | Libovolná platná hodnota Značka       | Neomezeno          |
| TV         | Velikost obrazovky              | 20″–80″                     | Neomezeno          |
| TV         | Svislé rozlišení      | 480i, 720p, 1080i nebo 1080p | 1080p         |
| TV         | Obnovovací frekvence obrazovky      | 60 Hz, 120 Hz nebo 240 Hz       | 60 Hz          |
| TV         | Vstupy HDMI              | 0–10                        | 3             |
| TV         | Vstupy DVI               | 0–10                        | 1             |
| TV         | Kompozitní vstupy         | 0–10                        | 2             |
| TV         | Komponentní vstupy         | 0–10                        | 1             |
| LCD        | Připraveno na 3D                 | Ano nebo Ne                   | Ano           |
| LCD        | 3D k dispozici               | Ano nebo Ne                   | Žádný            |
| Plazma     | Provozní teplota od      | 0–43 °C              | 32            |
| Plazma     | Provozní teplota do        | 0–43 °C              | 100           |
| Projekční | Záruka | 6, 12 nebo 18 měsíců         | 12            |
| Projekční | Počet trubic    | 1–5                         | 3             |


## <a name="attribute-type"></a>Typ atributu
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) 
  
Atributy jsou založeny na typech atributů. Typy atributů určují typ dat, který lze zadat pro určitý atribut. Aplikace Microsoft Dynamics 365 for Operations v současné době podporují následující typy atributů:

-   **Měna** – tento typ atributu podporuje měnové hodnoty. Mohou být vázané (může tedy podporovat rozsah hodnot), nebo mohou být otevřené.
-   **Datum a čas** – tento typ atributu podporuje hodnoty data a času. Mohou být vázané (může tedy podporovat rozsah hodnot), nebo mohou být otevřené.
-   **Desetinné číslo** – tento typ atributu podporuje číselné hodnoty, které obsahují desetinná místa. Podporuje také měrné jednotky. Mohou být vázané (může tedy podporovat rozsah hodnot), nebo mohou být otevřené.
-   **Celé číslo** – tento typ atributu podporuje číselné hodnoty. Podporuje také měrné jednotky. Mohou být vázané (může tedy podporovat rozsah hodnot), nebo mohou být otevřené.
-   **Text** – tento typ atributu podporuje textové hodnoty. Podporuje také předdefinovanou sadu možných hodnot (výčtů).
-   **Logická hodnota** – tento typ atributu podporuje binární hodnoty (**pravda**/**nepravda**).
-   **Odkaz**.

## <a name="attribute"></a>Atribut
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) Kromě názvu, popisného názvu, popisu a textu nápovědy lze zaznamenat pro atribut jeden nebo více z následujících typů informací:

-   Výchozí hodnota
-   Metadata atributu, jako jsou například metadata, která určují, zda lze atributu vyhledávat, upřesňovat a řadit

## <a name="attribute-group"></a>Skupina atributů
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Po definování lze atributy seskupovat do skupin atributů. Skupiny atributů poskytují seskupení jednotlivých atributů a mohou být přiřazeny kategoriím maloobchodu nebo maloobchodním sítím.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Přiřazení skupin atributů ke kategoriím maloobchodu
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Jednu nebo více skupin atributů lze přiřadit k uzlům kategorií v hierarchii kategorií produktů maloobchodu. Po zařazení produktů do kategorií, zdědí produkty atributy, které jsou zahrnuty ve skupinách atributů.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Přiřazení skupin atributů k maloobchodním prodejnám
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Jednu nebo více skupin atributů lze přiřadit k jedné nebo více maloobchodním prodejnám v hierarchii maloobchodních prodejen. Po upravení produktů pro konkrétní maloobchodní prodejny, zdědí produkty atributy, které jsou zahrnuty ve skupinách atributů.

## <a name="overriding-attribute-values"></a>Přepsání hodnot atributů
### <a name="at-the-product-level"></a>Na úrovni produktu

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) Výchozí hodnoty atributů lze přepsat na úrovni produktu (tedy pro jednotlivé výrobky).

### <a name="in-a-retail-catalog"></a>V maloobchodním katalogu

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) Výchozí hodnoty atributů lze přepsat pro jednotlivé produkty v určitých katalozích, které jsou určeny pro konkrétní maloobchodní sítě.

### <a name="at-the-retail-channel-level"></a>Na úrovni maloobchodní sítě

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) Výchozí hodnoty atributů lze přepsat pro jednotlivé produkty v určitých katalozích, které jsou určeny pro konkrétní maloobchodní sítě.





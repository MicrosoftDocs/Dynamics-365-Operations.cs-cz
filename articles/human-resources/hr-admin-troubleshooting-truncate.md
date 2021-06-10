---
title: Zabránění zkrácení textu na hierarchii pozic a export do aplikace Visio
description: Tento článek vysvětluje, jak vyřešit problém, kdy jsou názvy osob a pozic zkráceny při odběratelově zobrazení hierarchie pozic v aplikaci Microsoft Dynamics 365 Human Resources. Zkrácení textu může ztížit pořízení snímku obrazovky nebo tisk hierarchie.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a03c8f340e8ebb2fb0440518c154ed3bdd0197f6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053244"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Zabránění zkrácení textu na hierarchii pozic a export do aplikace Visio

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Výdej**

Když si zákazník zobrazí hierarchii pozic v aplikaci Microsoft Dynamics 365 Human Resources, názvy osob a pozic jsou zkráceny. Z tohoto důvodu může být obtížné provést snímek obrazovky, nebo vytisknout a rozdělit hierarchii.

![Hierarchie pozic](media/position-h.png)

**Příčina**

Toto chování je záměrné.

**Řešení**

Bohužel uživatelé nemohou snadno změnit velikost textu. Můžete však exportovat hierarchii pozic mimo aplikaci Human Resources a potom ji importovat do aplikace Microsoft Visio. Ačkoli je následující článek určen pro aplikaci Microsoft Dynamics AX 2012, proces platí i pro Human Resources: [Exportovat hierarchii pozic do aplikace Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Tento postup slouží k exportu do aplikace Visio.

1. V modulu Lidské zdroje otevřete stránku se seznamem **pozic**.

    Chcete-li do diagramu struktury organizace zahrnout další informace, přidejte pole do seznamu **Pozice**, aby byly k dispozici při použití tohoto průvodce později v tomto postupu.

2. V podokně akcí, vyberte tlačítko **Otevřít v aplikaci Microsoft Office** a poté v nabídce **Exportovat do aplikace Excel** vyberte **Pozice**. Případně stiskněte Ctrl+T.

    ![Export stránky se seznamem Pozice do aplikace Excel](media/org-admin.png)

3. Uložte soubor aplikace Excel, který je vyexportovaný.

    ![Export do dialogového okna Excelu](media/export-excel.png)

4. V aplikaci Visio vyberte **Visio – Vytvořit novou** a vyberte kategorii šablony **Obchodní**.

    ![Nový diagram](media/new.png)

5. Vyberte **Průvodce grafem organizace** a poté vyberte **Vytvořit**.

    ![Dialogové okno průvodce grafem organizace](media/orgchart-wizard.png)

6. Vyberte **Informace, které jsou již uložené v souboru nebo databázi** a poté vyberte **Další**.

    ![Průvodce grafem organizace 1](media/orgchart-wizard7.png)

7. Zvolte **Text, Org Plus (\*.txt), nebo soubor aplikace Excel** a poté zvolte **Další**.

    ![Průvodce grafem organizace 2](media/orgchart-wizard3.png)

8. Vyhledejte exportovaný soubor aplikace Excel, který obsahuje hierarchii pozic, a poté vyberte **Další**.

    ![Průvodce grafem organizace 3](media/orgchart-wizard2.png)

9. Nastavte pole **Název** na **pozice**, nastavte pole **Nadřízená pozice** na **Podřízený pozice** a poté vyberte **Další**.

    ![Průvodce grafem organizace 4](media/orgchart-wizard1.png)

10. Vyberte pole, která mají být zobrazena na každém uzlu, a poté vyberte **Další**.

    ![Průvodce grafem organizace 5](media/orgchart-wizard5.png)

11. Přidejte sloupec **Pozice** do seznamu **Pole vlastností obrazce** a pak vyberte **Další**.

    ![Průvodce grafem organizace 6](media/orgchart-wizard6.png)

12. Obrázky nejsou v současné době k dispozici. Proto na další stránce vyberte **Další**.
13. Vyberte **Chci, aby průvodce automaticky rozdělil organizační schéma mezi stránky**.

    ![Průvodce grafem organizace 7](media/orgchart-wizard4.png)

14. Vyberte **Dokončit**.

    Pokud existují nějaké pozice, které nejsou ve struktuře, budete vyzváni k jejich zařazení do schématu.

Diagram, který se vygeneruje v aplikaci Visio, zobrazuje každého manažera v samostatném listu.

Na základě polí, která jste vybrali do schématu, každý uzel zobrazí příslušné informace při generování souboru Visio.

![Diagram hierarchie](media/hierarchy.png)

**Další možnost**

V aplikaci Human Resources můžete rovněž použít pracovní prostor **Osoby** pro zobrazení některých informací souvisejících s hierarchií.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Import katalogů dodavatele
description: Toto téma popisuje proces importu dat katalogu dodavatele.
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 608d2b57bb4d5ab80d75b22ed5c8a4df5263e5f3
ms.sourcegitcommit: 86052c58e3c365c443bd6f37ad1054bea395e21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2020
ms.locfileid: "3338301"
---
# <a name="import-vendor-catalogs"></a>Import katalogů dodavatele

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Import katalogů dodavatele

V aplikaci Dynamics 365 Supply Chain Management mohou nakupující profesionálové vytvářet a udržovat katalogy, které zaměstnanci společnosti mohou použít při objednání položek a služeb pro interní použití. Chcete-li vytvořit zásobovací katalog, můžete přidat položky a služby, které chcete zpřístupnit zaměstnancům, buď importem dat katalogu produktů nebo ručním přidáním dat katalogu produktů do základního produktu. 

Můžete načíst data katalogu odeslaná dodavatelem z klienta aplikace Microsoft Dynamics 365.

Data produktu, které vám dodavatel odešle ve formě souboru požadavku na údržbu katalogu (CMR), musí být ve formátu XML. Soubor CMR by měl obsahovat podrobné informace o produktech, které dodavatel poskytuje vaší společnosti.

## <a name="import-vendor-catalog-data"></a>Import dat katalogů dodavatele

Chcete-li importovat data katalogu dodavatele, je nutné provést následující úkoly:

1. Nastavte projekt v pracovním prostoru Správa dat, kde jste definovali pravidla mapování dat. Vyberte **Správa dat** a poté vyberte **Nastavit role pro datové projekty**.

2. Nastavte hierarchii kategorií zásobování a přiřaďte své dodavatele do kategorií zásobování. Při použití kódů komodit přidejte kódy komodit do kategorií zásobování. Informace o nastavení hierarchie kategorií zásobování naleznete v tématu [Nastavení hierarchie kategorií zásobování](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3. Konfigurujte dodavatele pro import katalogu. Vyberte dodavatele a poté vyberte **Zásobování** > **nastavit** > **Konfigurovat dodavatele pro importu katalogu**.

4. Nakonfigurujte workflow pro import katalogu. Vytvořte šablonu souboru CMR a nasdílejte ji se svým dodavatelem.

5. Vyberte **Zásobování a zdroje** \> **Společné** \> **Katalogy** \> **Katalogy dodavatele** a vytvořte katalog dodavatele. Soubory požadavku na údržbu katalogu (CMR), které jste přijali od dodavatele, jsou seskupeny v tomto katalogu. 

6. Odešlete soubor CMR.

7. Zrevidujte, schvalte nebo zamítněte produkty v katalogu dodavatele. Produkty jsou automaticky přiřazeny do kategorie zásobování. 

Schválené produkty jsou přidány do základního produktu a jsou uvolněny pro vybrané právnické osoby. Pouze schválené produkty lze přidat do zásobovacího katalogu.

## <a name="generate-a-catalog-import-file-template"></a>Generování šablony souboru pro import katalogu

Soubor šablony pro import katalogu je soubor průmyslového standardu XSD, který použijete k vytvoření souboru CMR pro produkty dodavatele. Můžete použít soubor CMR pro vytvoření nového katalogu, nahrazení existujícího katalogu nebo úpravě existujícího katalogu.

1. Vyberte **Zásobování a zdroje** \> **Katalogy** \> **Katalogy dodavatele** a dvakrát klikněte na katalog, se kterým chcete pracovat.

2. Stáhněte aktuální šablonu importu katalogu (soubor XSD). Na stránce **Aktualizovat katalog** v **podokně akcí**na kartě **Katalogy** ve skupině **Související informace** klikněte na **Generovat šablonu katalogu** a vyberte **Kategorie zásobování**.

    - S možností **Kategorie zásobování** můžete generovat šablonu katalogu, která obsahuje kategorie zásobování, ve které je dodavatel oprávněn poskytovat produkty.

3. V dialogovém okně **Uložit jako** vyberte umístění, do kterého chcete šablonu souboru s katalogem uložit a soubor uložte.

Další informace a příklady naleznete v tomto příspěvku blogu: [Katalogy dodavatele v aplikaci Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).

---
title: "Prodejní objednávky mobilní pracovní prostor pro Microsoft Dynamics 365 pro provoz aplikace"
description: "S mobilním prostoru prodejní objednávky zůstali aktuálních prodejních objednávek kdekoli a kdykoli."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 31
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Prodejní objednávky mobilní pracovní prostor pro Microsoft Dynamics 365 pro provoz aplikace

S mobilním prostoru prodejní objednávky zůstali aktuálních prodejních objednávek kdekoli a kdykoli. 

<a name="prerequisites"></a>Předpoklady
-------------

| Předpoklad                                                         | popis                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přečtěte si informace o Microsoft Dynamics 365 pro provoz mobilní platformu | [Dynamics 365 pro mobilní platformu operace](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 pro operace                                          | Ujistěte se, že používáte prostředí, které má Microsoft Dynamics 365 pro verzi operace 1611 a Microsoft Dynamics pro operace platformy aktualizace 3 (listopad 2016). |
| Opravy hotfix KB 3215650                                                    | Nainstalujte opravu hotfix Chcete-li povolit pracovní prostory, které jsou součástí Microsoft Dynamics 365 pro operace.                                                                       |
| Mobilní zařízení, které má 365 Dynamics pro operace aplikace nainstalována | Stáhněte 365 Dynamics pro operace aplikace z úložiště vaše mobilní aplikace.                                                                                                      |

## <a name="overview"></a>Přehled
Tento mobilní pracovní prostor přistupuje k 365 Dynamics operací aplikace a umožňuje zobrazit podrobné informace o jednotlivých prodejních objednávkách, například stav objednávky, informace o kontaktu zákazníka a kontaktní informace pro příjemce objednávky. Mobilní pracovní prostor poskytuje okamžitý přehled o prodejních objednávkách. Zobrazit prodejní objednávky podle zákazníka, nebo zobrazit všechny prodejní objednávky nebo zobrazení informací o konkrétní prodejní objednávku. Mobilní pracovní prostor obsahuje dvě zobrazení, které vám umožní analyzovat prodejní objednávky do hloubky.

### <a name="view-all-sales-orders"></a>Zobrazit všechny prodejní objednávky

Toto zobrazení obsahuje seznam všech prodejních objednávek.

-   Použijte jeden z následujících filtrů vyberte prodejní objednávky, které chcete zobrazit.
    -   Hledat podle prodejní objednávky
    -   Hledání podle účtu odběratele
    -   Hledat podle jména zákazníka
    -   Hledání podle stavu
    -   Hledání podle stavu uvolnění
    -   Hledat datum a čas vytvoření

<!-- -->

-   Po výběru prodejní objednávky můžete zobrazit podrobnosti o konkrétní objednávky. Konkrétně můžete zobrazit:
    -   Informace o názvu a adresy odběratele
    -   Data různých prodejních objednávek jako požadované datum expedice a potvrzené datum expedice
    -   Kontaktní informace pro příjemce objednávky
    -   Informace o kontaktu zákazníka
    -   Řádky objednávky
    -   Dodávky, které ukazují, jak a kdy byla prodejní objednávka dodána

### <a name="view-orders-for-a-customer-"></a>Zobrazit objednávky pro zákazníka ** **

Toto zobrazení obsahuje seznam prodejních objednávek podle odběratele.

-   Chcete-li zobrazit objednávky pro zákazníka, použijte jednu z následující filtry.
    -   Hledání podle názvu
    -   Hledání podle účtu

<!-- -->

-   Po výběru zákazníka můžete zobrazit:
    -   Jméno zákazníka a skupiny
    -   Informace o kontaktu zákazníka
    -   Prodejní objednávky zákazníka a podrobnosti prodejní objednávky:
        -   Informace o názvu a adresy odběratele
        -   Kalendářní data v různých prodejních objednávek
        -   Kontaktní informace pro příjemce objednávky
        -   Informace o kontaktu zákazníka
        -   Řádky objednávky
        -   Dodávky, které ukazují, jak a kdy bylo dodáno prodejních objednávek

## <a name="get-started"></a>Začínáme
Postupujte při seznamování s mobilním prostoru prodejní objednávky v mobilním zařízení.

1.  V úložišti mobilní aplikace stáhnout a nainstalovat 365 Microsoft Dynamics pro operace app.
2.  Spuštění aplikace v zařízení.
3.  Zadejte adresu URL aplikace Dynamics 365.
4.  Zadejte přihlášení do společnosti. Například zadejte **USMF**.
5.  Při prvním přihlášení, budete vyzváni pro uživatelské jméno a heslo pro vaše 365 Microsoft Dynamics pro účet operací. Zadejte svá pověření. Po přihlášení, zobrazí se dostupné pracovní prostory pro vaši firmu.

Zobrazení pracovní plochy na mobilní aplikace, musíte nejprve publikovat požadované pracovní prostory do 365 Dynamics pro operace app.

1.  Spusťte Dynamics 365 pro operace.
2.  Přejít na **Správa systému**&gt;**nastavení**&gt;**parametry systému**.
3.  Vyberte **Správa mobilní aplikace**.
4.  Vyberte pracovní prostor k publikování na mobilní platformy.
5.  Vyberte **publikovat pracovního prostoru**.
6.  Aktualizujte zařízení zobrazit publikované pracovní prostory.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Zobrazení informací o prodejní objednávky pro zákazníka
1.  V mobilním zařízení, vyberte **prodejní objednávky** prostoru.
2.  Vyberte **zobrazit objednávky pro zákazníka,**.
3.  Použití ** účtu ** nebo ** jméno zákazníka ** informace k nalezení požadovaného zákazníka.
4.  Vyberte odběratele.
5.  Vyberte **kontaktní informace** nebo **prodejní objednávky**.
6.  Pokud **prodejní objednávky** je vybrali, se zobrazí seznam prodejních objednávek pro zákazníka.
7.  Vyberte **prodeje**.
8.  Zde můžete zobrazit informace o řádcích prodejní objednávky, dodávky, kontaktní informace zákazníka a kontaktní informace pro příjemce objednávky.





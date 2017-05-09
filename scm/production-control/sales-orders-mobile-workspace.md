---
title: "Mobilní pracovní prostor prodejních objednávek pro aplikaci Microsoft Dynamics 365 for Operations"
description: "S mobilním pracovním prostorem prodejních objednávek můžete mít stále aktuální přehled o svých prodejních objednávkách kdekoli a kdykoli."
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

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilní pracovní prostor prodejních objednávek pro aplikaci Microsoft Dynamics 365 for Operations

S mobilním pracovním prostorem prodejních objednávek můžete mít stále aktuální přehled o svých prodejních objednávkách kdekoli a kdykoli. 

<a name="prerequisites"></a>Předpoklady
-------------

| Předpoklad                                                         | popis                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přečtěte si o mobilní platformě Microsoft Dynamics 365 for Operations | [Mobilní platforma Microsoft Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Ujistěte se, že používáte prostředí, které má Microsoft Dynamics 365 for Operations verzi 1611 a aktualizaci platformy Microsoft Dynamics for Operations 3 (listopad 2016). |
| Oprava KB 3215650                                                    | Nainstalujte opravu hotfix, abyste povolili pracovní prostory, které jsou součástí Microsoft Dynamics 365 for Operations.                                                                       |
| Mobilní zařízení, které má nainstalovanou aplikaci Dynamics 365 for Operations | Stáhněte aplikaci Dynamics 365 for Operations z vašeho obchodu mobilních aplikací.                                                                                                      |

## <a name="overview"></a>Přehled
Tento mobilní pracovní prostor přistupuje k aplikaci Dynamics 365 for Operations a umožňuje zobrazit podrobné informace o jednotlivých prodejních objednávkách, například stav objednávky, informace o kontaktu zákazníka a kontaktní informace pro příjemce objednávky. Mobilní pracovní prostor poskytuje okamžitý přehled o prodejních objednávkách. Můžete zobrazit prodejní objednávky podle zákazníka nebo zobrazit všechny prodejní objednávky o konkrétní prodejní objednávce. Mobilní pracovní prostor obsahuje dvě zobrazení, která vám umožní analyzovat prodejní objednávky do hloubky.

### <a name="view-all-sales-orders"></a>Zobrazit všechny prodejní objednávky

Toto zobrazení obsahuje seznam všech prodejních objednávek.

-   Použijte jeden z následujících filtrů pro výběr prodejních objednávek, které chcete zobrazit.
    -   Hledat podle prodejní objednávky
    -   Hledat podle odběratele
    -   Hledat podle jména odběratele
    -   Hledat podle stavu
    -   Hledat podle stavu storna
    -   Hledat podle data a času vytvoření

<!-- -->

-   Po výběru prodejní objednávky můžete zobrazit podrobnosti o konkrétní objednávce. Konkrétně můžete zobrazit:
    -   Informace o názvu a adrese zákazníka
    -   Data různých prodejních objednávek jako požadované datum expedice a potvrzené datum expedice
    -   Kontaktní informace objednatele
    -   Kontaktní informace odběratele
    -   Řádky objednávky
    -   Dodávky, které ukazují, jak a kdy byla prodejní objednávka dodána

### <a name="view-orders-for-a-customer-"></a>Zobrazení objednávek pro odběratele** **

Toto zobrazení uvádí seznam prodejních objednávek na odběratele.

-   Chcete-li zobrazit objednávky pro odběratele, použijte jeden z následujících filtrů.
    -   Hledat podle jména
    -   Hledat podle účtu

<!-- -->

-   Po výběru zákazníka můžete zobrazit:
    -   Název skupinu odběratelů
    -   Kontaktní informace odběratele
    -   Prodejní objednávky zákazníka a podrobnosti prodejní objednávky:
        -   Informace o názvu a adrese zákazníka
        -   Různá data prodejních objednávek
        -   Kontaktní informace objednatele
        -   Kontaktní informace odběratele
        -   Řádky objednávky
        -   Dodávky, které ukazují, jak a kdy byly prodejní objednávky dodány

## <a name="get-started"></a>Začínáme
Abyste mohli začít používat mobilní pracovní prostor prodejních objednávek na svém mobilním zařízení, postupuje podle následujících kroků.

1.  Stáhněte aplikaci Microsoft Dynamics 365 for Operations z obchodu mobilních aplikací.
2.  Spusťte aplikaci na svém zařízení.
3.  Zadejte adresu URL aplikace Dynamics 365.
4.  Zadejte společnost, do které se chcete přihlásit. Například zadejte **USMF**.
5.  Při prvním přihlášení budete vyzváni k zadání uživatelského jména a hesla pro váš účet aplikace Microsoft Dynamics 365 for Operations. Zadejte své přihlašovací údaje. Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost.

Pro zobrazení pracovního prostoru ve své mobilní aplikaci musíte nejprve publikovat požadovaný pracovní prostor do aplikace Dynamics 365 for Operations.

1.  Spusťte aplikaci Dynamics 365 for Operations.
2.  Přejděte do nabídky **Správa systému** &gt; **Nastavení** &gt; **systémových parametrů**.
3.  Zvolte **Spravovat aplikaci pro mobilní zařízení**.
4.  Vyberte pracovní prostor pro publikování na mobilní platformu.
5.  Vyberte **Publikovat pracovní prostor**.
6.  Aktualizujte zařízení pro zobrazení publikovaných pracovních prostorů.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Zobrazení informací o prodejních objednávkách pro určitého zákazníka
1.  Na svém mobilním zařízení vyberte pracovní prostor **Prodejní objednávky**.
2.  Vyberte **Zobrazení objednávek pro odběratele**
3.  Pomocí informací v poli Účet nebo Název zákazníka vyhledejte požadovaného zákazníka.
4.  Vyberte zákazníka.
5.  Vyberte **Kontaktní informace** nebo **Prodejní objednávky**.
6.  Pokud je vybraná možnost **Prodejní objednávky**, zobrazí se seznam prodejních objednávek pro zákazníka.
7.  Vyberte **Prodejní objednávka**.
8.  Zde můžete zobrazit informace o řádcích prodejní objednávky, dodávkách, kontaktní informace zákazníka a kontaktní informace příjemce objednávky.





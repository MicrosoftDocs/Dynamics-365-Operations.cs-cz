---
title: "Mobilní pracovní prostor řízení nákladů pro aplikaci Microsoft Dynamics 365 for Operations"
description: "Díky mobilnímu pracovní prostoru řízení nákladů mohou manažeři nákladových středisek kdykoliv a kdekoliv vidět výkonnost středisek."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilní pracovní prostor řízení nákladů pro aplikaci Microsoft Dynamics 365 for Operations

Díky mobilnímu pracovní prostoru řízení nákladů mohou manažeři nákladových středisek kdykoliv a kdekoliv vidět výkonnost středisek. 

<a name="prerequisites"></a>Předpoklady
-------------

| Předpoklad                                                         | popis                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přečtěte si o mobilní platformě Microsoft Dynamics 365 for Operations | [Mobilní platforma Microsoft Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Ujistěte se, že používáte prostředí, které má Microsoft Dynamics 365 for Operations verzi 1611 a Microsoft Dynamics for Operations aktualizaci platformy 3 (listopad 2016). |
| Oprava KB 3215650                                                    | Nainstalujte opravu hotfix, abyste povolili pracovní prostory, které jsou součástí Microsoft Dynamics 365 for Operations.                                                                       |
| Mobilní zařízení, které má nainstalovanou aplikaci Dynamics 365 for Operations | Stáhněte aplikaci Dynamics 365 for Operations z vašeho obchodu mobilních aplikací.                                                                                                      |

## <a name="introduction"></a>Úvod
Mobilní pracovní prostor řízení nákladů poskytuje okamžitý přehled o aktuálním výkonu nákladových středisek porovnáním skutečných nákladů s rozpočtovými náklady. Můžete přejít na stavy jednotlivých prvků nákladů.

### <a name="example"></a>Příklad

Zaměstnanec obdrží pozvánku na mezinárodní konferenci. Organizace bude muset pokrýt všechny cestovní výdaje. Zaměstnanec se zeptá svého manažera, zda se může konference zúčastnit. Manažer rychle otevře mobilní pracovní prostor řízení nákladů na svém mobilním telefonu a zjistí, zda má rozpočet pro zaměstnance k účasti na konferenci.

### <a name="data-security"></a>Zabezpečení dat

Data v pracovním prostoru řízení nákladů jsou zabezpečena pomocí pověření uživatele. Pouze manažer nákladového střediska může vidět data pro své nákladové středisko. Úroveň zabezpečení přístupu je spravována v rámci modulu Nákladové účetnictví. Účetní definují konfiguraci mobilního pracovního prostoru řízení nákladů v modulu Nákladové účetnictví. Po publikování pracovního prostoru do aplikace Microsoft Dynamics 365 for Operations bude v aplikaci pracovní prostor k dispozici. Tím zajistíte, že všichni manažeři nákladových středisek v organizaci uvidí data ve stejném formátu.

### <a name="actions-views-and-links"></a>Akce, zobrazení a odkazy

Mobilní pracovní prostor řízení nákladů pro aplikaci Dynamics 365 for Operations nabízí následující akce, zobrazení a odkazy:

-   Akce 
    -   Pro výběr rozvržení zvolte položku **Konfigurace**.
    -   Zvolte **Nákladové objekty** a vyberte nákladová střediska, na kterých chcete filtrovat data. **Poznámka:** Zobrazí se seznam podle přístupu uděleného v modulu Nákladové účetnictví.

<!-- -->

-   Podle toho, co je zvoleno pod možností **Akce** a co je nakonfigurováno v modulu Nákladové účetnictví, můžete zobrazit následující informace v kartách. Všimněte si, že částka je zobrazena ve stejném formátu: skutečná, rozpočet, odchylka a % odchylky. 
    -   Skutečnost vs. rozpočet (aktuální období)
    -   Skutečný vs. revidovaný rozpočet (aktuální období)
    -   Skutečnost vs. rozpočet (předchozí období)
    -   Skutečný vs. revidovaný rozpočet (předchozí období)
    -   Skutečnost vs. rozpočet (od začátku roku)
    -   Skutečný vs. revidovaný rozpočet (od začátku roku)

<!-- -->

-   Odkazy
    -   Podrobnosti za aktuální období.
    -   Podrobnosti za předchozí období.
    -   Podrobnosti za období od začátku roku.

Když vyberete jeden z odkazů, zobrazí se karta podle prvku nákladů. Částka v kartách se zobrazí v následujícím formátu: skutečnost, rozpočet, odchylka rozpočtu, % odchylky rozpočtu, revidovaný rozpočet, odchylka revidovaného rozpočtu a % odchylky revidovaného rozpočtu.  [![Řízení nákladů](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Začínáme
Abyste mohli začít používat mobilní aplikaci řízení nákladů na svém mobilním zařízení, postupuje podle následujících kroků.

1.  Stáhněte aplikaci Dynamics 365 for Operations z vašeho obchodu mobilních aplikací.
2.  Spusťte aplikaci na svém zařízení.
3.  Zadejte adresu URL aplikace Dynamics 365.
4.  Zadejte společnost, do které se chcete přihlásit. Například zadejte **USMF**.
5.  Při prvním přihlášení budete vyzváni k zadání uživatelského jména a hesla pro váš účet aplikace Microsoft Dynamics 365 for Operations. Zadejte své přihlašovací údaje. Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost.

Pro zobrazení pracovního prostoru ve své mobilní aplikaci musíte nejprve publikovat požadovaný pracovní prostor do aplikace Dynamics 365 for Operations.

1.  Spusťte aplikaci Dynamics 365 for Operations.
2.  Přejděte do nabídky **Správa systému** &gt; **Nastavení** &gt; **systémových parametrů**.
3.  Zvolte **Spravovat aplikaci pro mobilní zařízení**.
4.  Vyberte pracovní prostor ** Řízení nákladů** pro publikování na mobilní platformu.
5.  Vyberte **Publikovat pracovní prostor**.
6.  Aktualizujte zařízení pro zobrazení publikovaných pracovních prostorů.

## <a name="view-the-performance-of-your-cost-center"></a>Zobrazení výkonu vašeho nákladového střediska
1.  Na svém mobilním zařízení vyberte pracovní prostor **Řízení nákladů**.
2.  Vyberte **Řízení objektu nákladů**.
3.  Klikněte na **Akce**.
4.  Klikněte na tlačítko **Zvolit konfiguraci** a vyberte rozvržení řízení nákladů.
5.  Klikněte na tlačítko **Hotovo**.
6.  Klikněte na **Akce**.
7.  Klikněte na tlačítko **Zvolit objekt nákladů** a vyberte nákladová střediska, ke kterým vám byl udělen přístup.
8.  Klikněte na tlačítko **Hotovo**.
9.  Zobrazte celkovou výkonnost vašeho nákladového střediska.
10. Klikněte na **Podrobnosti za aktuální období**.
11. Zobrazte výkonnost jednotlivých prvků nákladů.
12. Můžete také vyhledat konkrétní prvky nákladů.




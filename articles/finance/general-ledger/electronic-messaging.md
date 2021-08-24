---
title: Elektronické zprávy
description: Toto téma poskytuje přehled a informace o nastavení pro elektronické zprávy v Microsoft Dynamics 365 Finance.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 191abc37b7c349aaf3c9e871fe2f1885eec9fc896271d6fac27e5caa0b0fe3b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768332"
---
# <a name="electronic-messaging"></a>Elektronické zprávy

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled a informace o nastavení pro funkci **elektronických zpráv** (EM).

Nedávno vlády a legislativní orgány různých zemí a regionů na celém světě zavedly požadavky na podávání zpráv pro společnosti, které jsou registrovány v těchto zemích nebo regionech. Účelem požadavků je umožnit získávání údajů z těchto společností v elektronickém formátu přímo ze systémů, kde byly účtovány, uloženy a zpracovány.

Funkce elektronických zpráv v aplikaci Microsoft Dynamics 365 Finance podporuje různé procesy elektronické spolupráce mezi aplikací Finance a systémy, které vlády a legislativní orgány nabízejí pro podávání zpráv, předkládání a přijímání oficiálních informací.

Funkce elektronických zpráv je integrována s modulem **Elektronického výkaznictví**. Můžete nastavit formáty elektronického výkaznictví pro elektronické zprávy. Další informace získáte v tématu [Elektronické výkaznictví](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>Základní koncepty pro funkci EM

Funkce EM je založena na následujících entitách:

- **Elektronická zpráva** – Hlášení nebo prohlášení, které by mělo být hlášeno nebo předáno interně, například hlášení zaslané finančnímu úřadu.
- **Položky elektronických zpráv** – Záznamy, které mají být zahrnuty ve vykazované zprávě.
- **Zpracování elektronické zprávy** – Sled akcí, buď propojený nebo odpojený, který by měl být spuštěn pro shromažďování požadovaných dat, generování sestav, ukládání dat do úložiště Azure Blob, přenos sestav mimo systém, získání odpovědí mimo systém a aktualizace databáze. Akce v řetězci mohou být propojeny nebo nepropojeny.

Následující obrázek znázorňuje tok dat pro EM.

![Tok dat elektronických zpráv.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>Scénáře podporované funkcí EM

Funkce elektronických zpráv podporuje následující situace:

- Ruční vytváření zpráv a generování sestav založených na přidružených exportních formátech elektronického výkaznictví různých typů. Mezi tyto typy patří Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, text a Microsoft Word.
- Automatické vytvoření a zpracování zpráv, které jsou založeny na informacích požadovaných a přijatých od úřadu prostřednictvím přidruženého formátu importu elektronického výkaznictví.
- Sběr a zpracování informací z datového zdroje jako položek zprávy. Zdrojem dat je tabulka Finance.
- Ukládání dalších informací a vyhodnocování různých hodnot voláním specificky definovaných spustitelných tříd ve vztahu ke zprávám nebo položkám zpráv.
- Agregování informací, které jsou shromážděny v položkách zprávy, rozdělení těchto informací podle zprávy a generování sestav v přidružených exportních formátech elektronického výkaznictví.
- Přenesení sestav, které jsou generovány do webové služby pomocí informací o zabezpečení uložených v Azure Key Vault.
- Příjem odpovědi z webové služby, vyhodnocení odpovědi a aktualizace dat v aplikaci Finance podle potřeby.
- Uložení a kontrola všech sestav, které jsou generovány.
- Uložení a kontrola všech informací o protokolu, souvisejících s akcemi, které jsou spuštěny pro zprávy nebo položky zprávy.
- Kontrola zpracování pomocí různých stavů zpráv a položek zpráv.

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Regulační funkce specifické pro zemi podporované funkcí EM

Následující tabulka poskytuje informace o některých regulačních funkcích specifických pro danou zemi, které jsou podporovány funkcí EM.

| Země/oblast     | Název funkce | Nahrávání demo funkcí |
|-------------|--------------|------------------------|
| Španělsko       | [Okamžité poskytnutí informací o DPH (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Maďarsko     | [Online fakturační systém](../localizations/emea-hun-online-invoicing.md) | |
| Spojené království | [Digitalizování daní (MTD) – odeslání přiznání k DPH](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: Digitální daň Spojeného království – přiznání k DPH v Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litva   | [Hlášení i.SAF](../localizations/emea-ltu-isaf.md) | |
| Polsko      | [Přiznání k DPH s registry (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: Auditní rejstříky DPH SAF/JPK](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nizozemsko | [Přiznání k DPH pro Nizozemsko](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Česká republika | [Přiznání k DPH](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brazílie      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rusko      | [Přiznání k DPH](../localizations/rus-vat-declaration.md) | |
| Rusko      | [Vykazování účetnictví v elektronickém formátu](../localizations/rus-accounting-reporting.md) | |
| Rusko      | [Přiznání daně ze zisku](../localizations/rus-profit-tax-declaration.md) | |
| Rusko      | [Vyměřené daňové přiznání](../localizations/rus-assessed-tax-declaration.md) | |
| Rusko      | [Přiznání přepravní daně](../localizations/rus-transport-tax-declaration.md) | |
| Rusko      | [Přiznání daně z pozemku](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]


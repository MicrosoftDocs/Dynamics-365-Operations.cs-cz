---
title: Elektronické zprávy
description: Tento článek poskytuje přehled a informace o nastavení pro elektronické zprávy v Microsoft Dynamics 365 Finance.
author: liza-golub
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4e765c6d56e0ab6d209c27a70fd4b7e52273c103
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069873"
---
# <a name="electronic-messaging"></a>Elektronické zprávy

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled a informace o nastavení pro funkci **elektronických zpráv** (EM).

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

## <a name="security-privileges"></a>Oprávnění zabezpečení

Pro elektronické zprávy jsou k dispozici následující bezpečnostní oprávnění.

| Bezpečnostní oprávnění           | Úroveň přístupu | Přidružení |
|------------------------------|--------------|-------------|
| Udržovat elektronické zprávy | Toto oprávnění poskytuje plný přístup k funkcím EM. Pokud máte toto oprávnění, můžete nastavit elektronické zasílání zpráv a spustit veškeré zpracování. | Toto oprávnění je součástí povinnosti zabezpečení **Udržovat transakce DPH**. Tato povinnost je zase zahrnuta v roli zabezpečení **Účetní**. |
| Zobrazit elektronické zprávy     | Toto oprávnění poskytuje přístup k funkcím EM jen pro čtení. Pokud máte toto oprávnění, můžete zobrazit nastavení a zprávy pro elektronické zasílání zpráv. Nic však nemůžete nastavit ani spustit. | Toto oprávnění je součástí povinnosti zabezpečení **Dotaz na stav transakce DPH**. Tato povinnost je zase zahrnuta v následujících rolích zabezpečení:<ul><li>Manažer inkasa</li><li>Úředník pohledávek</li><li>Manažer pohledávek</li><li>Daňový účetní</li><li>Účetní</li><li>Účetní manažer</li><li>Účetní supervizor</li><li>Manažer prodeje</li><li>Úředník závazků</li></ul> |
| Provozování elektronických zpráv  | Toto oprávnění poskytuje přístup pouze na stránky **Elektronické zprávy** a **Položky elektronických zpráv**. Pokud máte toto oprávnění, můžete z těchto stránek spustit veškeré zpracování, které je voláno. | Toto oprávnění je součástí povinnosti zabezpečení **Provozovat elektronické zprávy**. Tato povinnost je zase zahrnuta v roli zabezpečení **Provozovatel elektronických zpráv**. |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Regulační funkce specifické pro zemi podporované funkcí EM

Následující tabulka poskytuje informace o některých regulačních funkcích specifických pro danou zemi, které jsou podporovány funkcí EM.

| Země/oblast     | Název funkce | Nahrávání demo funkcí |
|-------------|--------------|------------------------|
| Španělsko       | [Okamžité poskytnutí informací o DPH (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Maďarsko     | [Online fakturační systém](../localizations/emea-hun-online-invoicing.md) | |
| Spojené království | [Digitalizování daní (MTD) – odeslání přiznání k DPH](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance a provoz: Digitální přiznání DPH ve Velké Británii v Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litva   | [Hlášení i.SAF](../localizations/emea-ltu-isaf.md) | |
| Polsko      | [Přiznání k DPH s registry (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: Registry auditu DPH SAF/JPK](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nizozemsko | [Přiznání k DPH pro Nizozemsko](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Česká republika | [Přiznání k DPH](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brazílie      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rusko      | [Přiznání k DPH](../localizations/rus-vat-declaration.md) | |
| Rusko      | [Vykazování účetnictví v elektronickém formátu](../localizations/rus-accounting-reporting.md) | |
| Rusko      | [Přiznání daně ze zisku](../localizations/rus-profit-tax-declaration.md) | |
| Rusko      | [Vyměřené daňové přiznání](../localizations/rus-assessed-tax-declaration.md) | |
| Rusko      | [Přiznání přepravní daně](../localizations/rus-transport-tax-declaration.md) | |
| Rusko      | [Přiznání daně z pozemku](../localizations/rus-land-tax-declaration.md) | |
| Norsko      | [Vratka DPH s přímým odesláním do Altinn](../localizations/emea-nor-vat-return.md) | [Nová vratka DPH s přímým odesláním do Altinn v Dynamics 365 Finance](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| Francie      | [Přiznání k DPH (Francie)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| Rakousko     | [Přiznání k DPH (Rakousko)](../localizations/emea-aut-vat-declaration-austria.md) | |
| Německo     | [Přiznání k DPH (Německo)](../localizations/emea-deu-vat-declaration-germany.md) | |
| Nizozemsko | [Přiznání k DPH pro Nizozemsko](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Švédsko      | [Přiznání k DPH (Švédsko)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| Švýcarsko | [Přiznání k DPH (Švýcarsko)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]



---
title: Sdílení dat mezi společnostmi pro dárkové poukazy
description: Tento článek popisuje, jak nakonfigurovat aplikaci Microsoft Dynamics 365 Commerce k použití funkce sdílení dat Dynamics 365 Finance napříč datovými oblastmi k synchronizaci dat dárkových poukazů.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: bc0df6c4aac72907e8523069e3f1ae100780dc3c
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473924"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Sdílení dat mezi společnostmi pro dárkové poukazy

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nakonfigurovat aplikaci Microsoft Dynamics 365 Commerce k použití funkce sdílení dat Dynamics 365 Finance k synchronizaci dat dárkových poukazů. Funkci sdílení datových záznamů pak lze použít ke sdílení dat mezi společnostmi ve dvou datových oblastech. Tímto způsobem může interní tabulka dárkových poukazů Commerce sdílet data mezi dvěma entitami společnosti. Další informace o sdílení dat Dynamics 365 Finance mezi společnostmi naleznete v článku [Sdílení dat mezi společnostmi](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Klíčové podmínky

| Termín | Popis |
|---|---|
| Společnost | Právnická osoba v prostředí Dynamics 365 Finance. |
| Dárkový poukaz | Interní produkt dárkového poukazu Dynamics 365 Commerce. |

## <a name="prerequisites"></a>Předpoklady

Uživatelé musejí konfigurovat své prostředí pro sdílení dat mezi společnostmi, jak je popsáno v článku [Sdílení dat mezi společnostmi](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

Tabulka **RetailGiftCardTable** musí mít pole **DataSharingType** nastaveno na **Duplikát**, aby bylo povoleno sdílení duplicitních záznamů (DRS) pro tabulku dárkových poukazů. Více informací viz článek [Sdílení dat mezi společnostmi pro vývojáře](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Konfigurace sdílení dat mezi společnostmi pro dárkové poukazy

Při konfiguraci sdílení dat mezi společnostmi pro dárkové poukazy proveďte tyto kroky.

1. V Commerce headquarters přejděte na **Správa systému \> Nastavení \> Konfigurovat sdílení dat mezi společnostmi**.
1. V podokně Akce volbou **Nový** přidejte záznam sdílení dat.
1. V poli **Název** zadejte název záznamu sdílení dat (např. **Dárkové poukazy**).
1. V části **Tabulky a pole ke sdílení** sekce, vyberte **Přidat**.
1. V dialogovém okně **Sdílet novou tabulku** zadejte v poli **Název tabulky** hodnotu **RETAILGIFTCARDTABLE** (tabulka pro maloobchodní dárkové poukazy). Pole **Popisek tabulky** by mělo být automaticky nastaveno na **Tabulka dárkových poukazů**.
1. Ujistěte se, že jsou zaškrtnutá políčka **Uložit data podle společnosti**, **Má jedinečný index** a **Zatím nesdíleno** . Výběr těchto zaškrtávacích políček spustí ověření, která souvisejí s funkcí sdílení dat.
1. Zvolte **Přidat tabulku**. Záznam **Tabulka dárkových poukazů (RetailGiftCardTable)** by se nyní měl objevit v poli **Tabulky a pole ke sdílení**. Výběrem symbolu stříšky (^) zobrazíte všechna pole tabulky, která jsou automaticky přidružena k tabulce pro sdílení.
1. V části **Společnosti, které sdílí sestavy v těchto tabulkách** vyberte **Přidat** a přidejte společnost, se kterou chcete sdílet data.
1. V řádku pod polem **Společnost** vyberte společnost z rozevíracího seznamu.
1. Do pole **Název** zadejte název společnosti.
1. Opakováním kroků 8 až 10 přidejte další řádky společností.
1. Po dokončení přidávání řádků společnosti vyberte v podokně akcí možnost **Povolit**.
1. Zobrazí se varovná zpráva: „Doporučujeme tuto akci provádět pouze mimo pracovní dobu. Jakékoli operace souběžných transakcí pro tabulky v zásadě selžou. Chcete pokračovat?“ Potvrďte akci výběrem tlačítka **Ano**.
1. Zobrazí se varovná zpráva: „Přejete si nyní zkopírovat všechna stávající data mezi sdílenými společnostmi?“ Potvrďte akci výběrem tlačítka **Ano**.

Poté, co odsouhlasíte obě zprávy, začnou tabulky kopírovat data mezi konfigurovanými společnostmi. Zůstatky, které se objeví u jednoho firemního dárkového poukazu, pak uvidí druhá společnost.

## <a name="additional-resources"></a>Další prostředky

[Časté dotazy k platbám](payments-retail.md)

[Modul pokladny](../add-checkout-module.md)

[Platební modul](../payment-module.md)

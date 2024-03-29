---
title: Data faktur dodavatele
description: Tento článek popisuje data, která se objevují na fakturách dodavatele. Vysvětluje také, jak automaticky upravit datum zaúčtování.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 022fd0ce07fbb4c54afcf7334c1c9411e01dcf26
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775261"
---
# <a name="vendor-invoice-dates"></a>Data faktur dodavatele

[!include [banner](../includes/banner.md)]

Tento článek popisuje data, která se objevují na fakturách dodavatele. Vysvětluje také, jak automaticky upravit datum zaúčtování.

Na stránce **Podrobnosti čekající faktury dodavatele** se v záhlaví faktury zobrazí čtyři data: **Datum přijetí faktury**, **Datum faktury**, **Datum zaúčtování** a **Datum splatnosti**. Při vytvoření faktury dodavatele se standardně zadávají následující data:

- **Datum přijetí faktury** – Toto pole je nastaveno na aktuální systémové datum.
- **Datum zaúčtování** – Toto pole je nastaveno na aktuální systémové datum. 
- **Datum splatnosti** – Datum v tomto poli se vypočítá na základě data zaúčtování a platebních podmínek.
- **Datum faktury** – Ve výchozím nastavení je toto pole prázdné. Hodnotu v tomto poli však můžete podle potřeby zadat. V tomto případě je datum v poli **Datum splatnosti** přepočítáno na základě data faktury a platebních podmínek.

Někdy může být faktura dodavatele v nevyřízeném stavu po dlouhou dobu po uzávěrce období. Když je připravena k zaúčtování, stále se použije staré datum zaúčtování z minulého účetního období. Toto období je však nyní uzavřeno. Proto musí úředník pro závazky (AP) ručně změnit všechna data účtování na nové účetní období pro všechny nevyřízené faktury, které byly dříve vytvořeny.

Funkce popsaná v tomto článku vám umožňuje automaticky upravovat datum účtování podle obchodních požadavků.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parametr pro automatickou úpravu data zaúčtování dodavatelské faktury

Pro automatickou úpravu data účtování pro faktury dodavatele postupujte podle těchto kroků.

1.  Přejděte do nabídky **Závazky \> Nastavení \> Parametry závazků**.
2.  Na kartě **Hlavní kniha a DPH** v poli **Upravit datum zveřejnění automaticky** vyberte jednu z následujících hodnot:

    - **Žádná změna** – Systém během zaúčtování automaticky nemění datum zaúčtování. Tato hodnota je vybrána ve výchozím nastavení.
    - **Vždy změňte datum zaúčtování na systémové datum** – Datum zaúčtování se automaticky během zaúčtování změní na systémové datum.
    - **Změnit datum účtování na systémové datum, když je období data účtování uzavřeno nebo pozastaveno** – Během zaúčtování se automaticky změní datum zaúčtování na systémové datum, ale pouze v případě, že odpovídající období data zaúčtování má stav **Zavřeno** nebo **Blokováno**.
    - **Změnit datum účtování na první den nového období, když je období data účtování uzavřeno nebo pozastaveno** – Během zaúčtování se změní datum zaúčtování na pevný den nově otevřeného období, ale pouze v případě, že odpovídající období data zaúčtování má stav **Zavřeno** nebo **Blokováno**.

> [!NOTE]
> Pokud je nové datum zaúčtování, které bylo automaticky upraveno, v novém fiskálním roce, datum zaúčtování faktury se neaktualizuje. Uživatel uvidí chybu „Fiskální rok se změnil. Zkontrolujte a znovu zadejte datum zaúčtování." Aby bylo možné fakturu zaúčtovat, musí být aktualizováno datum zaúčtování do nového fiskálního roku.

## <a name="impact-of-posting-date-changes"></a>Dopad změn data zaúčtování

Když se změní datum zaúčtování na čekající faktuře dodavatele, má tato změna následující účinky:

- **Datum splatnosti**

    - Pokud je pole **Datum faktury** prázdné, datum splatnosti je přepočítáno na základě nového data zaúčtování a platebních podmínek.
    - Pokud bylo **Datum faktury** dříve nastaveno, změna data zaúčtování neovlivní datum splatnosti.

- **Dat. plat. slevy**

    - Pokud je pole **Datum faktury** prázdné, pro výpočet platební slevy se použije nové datum zaúčtování.
    - Pokud bylo pole **Datum faktury** dříve nastaveno, platební sleva se nezmění.

- **Směnný kurz** – Datum směnného kurzu je určeno nastavením možnosti **Aktualizovat účetnictví dodavatele pomocí data faktury** na kartě **Faktura** stránky **Parametry závazků** (**Závazky \> Nastavení \> Parametry závazků**).

    - Pokud je tato možnost nastavena na **Ano**, použije se **Datum faktury** a změna **Data zaúčtování** neovlivní směnný kurz.
    - Pokud je tato možnost nastavena na **Ne**, pro výpočet kurzu se použije datum zaúčtování. Při aktualizaci data účtování se přepočítají účetní a vykazované částky. Proto musí být ověření shody provedeno znovu.

## <a name="validation"></a>Ověření

Dvě další pole na kartě **Faktura** stránky **Parametry závazků** stránka (**Závazky \> Nastavení \> Parametry splatných účtů**) ovlivňují zpracování faktur:

- Pokud je pole **Zkontrolovat použité číslo faktury** je nastaveno na **Odmítnou duplikáty během fiskálního roku**, použije se datum zaúčtování ke kontrole duplicitních faktur během zaúčtování faktury.
- Pokud je pole **Vyžadovat datum dokladu na faktuře dodavatele** nastaveno na **Možnost chyby**, pole **Datum faktury v hlavičce čekající faktury** je vyžadováno. Pokud je datum faktury pozdější než datum zaúčtování, zobrazí se chybová zpráva.

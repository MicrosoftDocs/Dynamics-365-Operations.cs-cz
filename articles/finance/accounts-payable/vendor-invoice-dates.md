---
title: Data faktur dodavatele
description: Toto téma popisuje data, která se objevují na fakturách dodavatele. Vysvětluje také, jak nastavit systém tak, aby automaticky upravoval datum zaúčtování.
author: sunfzam
ms.date: 08/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: a066f828b47f297b8ad520b9eb0f4f311d49b111
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647878"
---
# <a name="vendor-invoice-dates"></a>Data faktur dodavatele

[!include [banner](../includes/banner.md)]

Toto téma popisuje data, která se objevují na fakturách dodavatele. Vysvětluje také, jak nastavit systém tak, aby automaticky upravoval datum zaúčtování.

Na stránce **Podrobnosti čekající faktury dodavatele** se v záhlaví faktury zobrazí čtyři data: datum přijetí faktury, datum faktury, datum zaúčtování a datum splatnosti. Při vytvoření faktury dodavatele se standardně zadávají následující data:

- **Datum přijetí faktury** – Toto pole je nastaveno na aktuální systémové datum.
- **Datum zaúčtování** – Toto pole je nastaveno na aktuální systémové datum. 
- **Datum splatnosti** – Datum v tomto poli se vypočítá na základě data zaúčtování a platebních podmínek.
- **Datum faktury** – Ve výchozím nastavení je toto pole prázdné. Hodnotu v tomto poli však můžete podle potřeby zadat. V tomto případě je datum v poli **Datum splatnosti** přepočítáno na základě data faktury a platebních podmínek.

Někdy může být faktura dodavatele v nevyřízeném stavu po dlouhou dobu po uzávěrce období. Když je připravena k zaúčtování, stále se použije staré datum zaúčtování z minulého účetního období. Toto období je však nyní uzavřeno. Proto musí úředník pro závazky (AP) ručně změnit všechna data účtování na nové účetní období pro všechny nevyřízené faktury, které byly dříve vytvořeny.

Funkce popsaná v tomto tématu vám umožňuje nastavit systém tak, aby automaticky upravoval datum účtování podle obchodních požadavků.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parametr pro automatickou úpravu data zaúčtování dodavatelské faktury

Chcete-li systému umožnit automatickou úpravu data účtování pro faktury dodavatele, postupujte podle těchto kroků.

1.  Přejděte do nabídky **Závazky \> Nastavení \> Parametry závazků**.
2.  Na kartě **Hlavní kniha a DPH** v poli **Upravit datum zveřejnění automaticky** vyberte jednu z následujících hodnot:

    - **Žádná změna** – Systém během zaúčtování automaticky nemění datum zaúčtování. Tato hodnota je vybrána ve výchozím nastavení.
    - **Vždy změňte datum zaúčtování na systémové datum** – Systém během zaúčtování automaticky změní datum zaúčtování na systémové datum.
    - **Změnit datum účtování na systémové datum, když je období data účtování uzavřeno nebo pozastaveno** – Systém během zaúčtování změní datum zaúčtování na systémové datum, ale pouze v případě, že odpovídající období data zaúčtování má stav **Zavřeno** nebo **Blokováno**.
    - **Změnit datum účtování na první den nového období, když je období data účtování uzavřeno nebo pozastaveno** – Systém během zaúčtování změní datum zaúčtování na pevní den nově otevřeného období, ale pouze v případě, že odpovídající období data zaúčtování má stav **Zavřeno** nebo **Blokováno**.

## <a name="impact-of-posting-date-changes"></a>Dopad změn data zaúčtování

Když se změní datum zaúčtování na čekající faktuře dodavatele, má tato změna následující účinky:

- **Datum splatnosti**

    - Pokud je pole **Datum faktury** prázdné, datum splatnosti je přepočítáno na základě nového data zaúčtování a platebních podmínek.
    - Pokud bylo **Datum faktury** dříve nastaveno, změna data zaúčtování neovlivní datum splatnosti.

- **Dat. plat. slevy**

    - Pokud je pole **Datum faktury** prázdné, pro výpočet platební slevy se použije nové datum zaúčtování.
    - Pokud bylo pole **Datum faktury** dříve nastaveno, platební sleva se nezmění.

- **Směnný kurz** – Datum směnného kurzu je určeno nastavením možnosti **Aktualizovat účetnictví dodavatele pomocí data faktury** na kartě **Faktura** stránky **Parametry závazků** (**Závazky \> Nastavení \> Parametry závazků**).

    - Pokud je tato možnost nastavena na **Ano**, použije se datum faktury a změna data zaúčtování neovlivní směnný kurz.
    - Pokud je tato možnost nastavena na **Ne**, pro výpočet kurzu se použije datum zaúčtování. Při aktualizaci data účtování se přepočítají účetní a vykazované částky. Proto musí být ověření shody provedeno znovu.

## <a name="validation"></a>Ověření

Dvě další pole na kartě **Faktura** stránky **Parametry závazků** stránka (**Závazky \> Nastavení \> Parametry splatných účtů**) ovlivňují zpracování faktur:

- Pokud je pole **Zkontrolovat použité číslo faktury** je nastaveno na **Odmítnou duplikáty během fiskálního roku**, systém používá datum zaúčtování ke kontrole duplicitních faktur během zaúčtování faktury.
- Pokud je pole **Vyžadovat datum dokladu na faktuře dodavatele** nastaveno na **Možnost chyby**, pole **Datum faktury v hlavičce čekající faktury** je vyžadováno. Pokud je datum faktury pozdější než datum zaúčtování, systém zobrazí chybové hlášení.

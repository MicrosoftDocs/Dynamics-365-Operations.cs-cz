---
title: Úložiště dat sledování splatnosti zákazníků
description: Tento článek popisuje proces používání externího úložiště pro sledování splatnosti odběratelů. Můžete spustit proces ukládání sledování splatnosti odběratelů a zpřístupnit výstup pro export do externího systému.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7a66485cc9a538f5c3999009b6dbe295d7a5b9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894135"
---
# <a name="customer-aging-data-storage"></a>Úložiště dat sledování splatnosti zákazníků

[!include [banner](../includes/banner.md)]

Tento článek popisuje proces používání externího úložiště pro sledování splatnosti odběratelů. V Microsoft Dynamics 365 Finance můžete spustit proces **ukládání sledování splatnosti** odběratelů a zpřístupnit výstup pro export do externího systému. Když proces spustíte, pro externí systémy jsou dostupné stejné možnosti sestavy sledování splatnosti, jaké jsou dostupné v systému. Podrobnosti jsou vždy zahrnuty v exportovaných datech.

Může být užitečné zpřístupnit sledování splatnosti odběratelů v externím systému pro uložení v případech, kdy výstup obsahuje mnoho zákazníků a/nebo mnoho transakcí. Pokud stávající sestava **Sledování splatnosti odběratele** vyprší, protože obsahuje příliš mnoho dat k tisku, tato funkce poskytuje alternativní způsob, jak získat stejná data.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Povolte funkci ukládání sledování splatnosti odběratelů

Než můžete použít tuto funkci, musíte ji povolit ve svém systému. Správci mohou pomocí nastavení správa funkcí zkontrolovat stav funkce a povolit ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** Kredit a inkasa
- **Název funkce:** Ukládání dat o sledování splatnosti odběratelů

## <a name="run-the-customer-aging-data-storage-process"></a>Soustťte proces ukládání dat o sledování splatnosti odběratelů

1. Přejděte do nabídky **Kredit a inkasa \> Dotazy a sestavy \> Platby \> Postdatované šeky odběratele**.
2. Zvolte **Nové**.
3. Do pole **Název** zadejte název procesu.
4. Zbývající parametry nastavte podle potřeby.

    > [!NOTE]
    > Podrobnosti transakce jsou vždy zahrnuty a zpracování se vždy provádí v dávkové úloze.

5. Vyberte **OK**.
6. Obnovte stránku **Úlžiště dat o sledování splatnosti odběratelů**, chcete-li zobrazit hodnoty **Název dávky** a **Doba běhu dávky**, které jsou zobrazeny společně s hodnotou **Stav zpracování**. Když je dávková úloha dokončena, pole **Stav zpracování** je nastaveno na **Skončeno** a pole **Počet řádků sledování splatnosti**. Pokud se dávková úloha opakuje, pole **Stav zpracování** je nastaveno na **Čekání**.
7. Vyberte tlačítko **Filtr** vedle pole **Počet řádků sledování splatnosti** pro kontrolu filtrů, které byly přidány pro dávkovou úlohu.

Stránka **Úložiště dat o sledování splatnosti zákazníků** neobsahuje výsledky. Datová entita **Úložiště dat o sledování splatnosti** umožňuje exportovat výstup do libovolného formátu, který správa dat podporuje.

> [!NOTE]
> Než provedete export, přidejte filtr, který omezí exportované výsledky na nejnovější sledování splatnosti. Například přidáním následujících kritérií vrátíte poslední spuštění dávky:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchName())
>
> Případně, přidáním následujících kritérií vrátíte poslední spuštění dávky pro aktuálního uživatele:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchNameForCurrentUser())

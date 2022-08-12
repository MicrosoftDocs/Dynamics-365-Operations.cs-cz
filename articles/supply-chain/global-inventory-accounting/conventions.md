---
title: Konvence
description: Tento článek popisuje, jak nastavit konvence pro stanovení způsobu účtování nákladů v Globálním účetnictví zásob.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f148d4c6ece543c8a11eee3e6dcdff47b3767936
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135493"
---
# <a name="conventions"></a>Konvence

[!include [banner](../includes/banner.md)]

Konvence je kontejner pro sadu zásad, které ovlivňují chování systému. Na základě vašich obchodních požadavků musíte definovat konvence pomocí kombinace různých zásad, které určují, jak by měly být náklady účtovány v globálním účetnictví zásob. Každou konvenci můžete přidružit k jedné nebo více knih, abyste zajistili konzistenci v účetních zásadách, které se používají mezi knihami.

Chcete-li nastavit své konvence, přejděte na **Globální účtování zásob \> Založit \> Konvence**. U každé konvence je třeba nastavit tato pole:

- **Název** – Zadejte název konvence.
- **Popis** - Zadejte popis konvence.
- **Zásady nákladových objektů** - Vyberte zásadu nákladového objektu. Tyto zásady určují úroveň podrobnosti, kterou systém používá k výpočtu a udržování hodnoty zásob. K dispozici jsou následující předdefinované možnosti:

    - Produkt
    - Produkt - web
    - Produkt - Web - Sklad

    Například pokud vyberete *Produkt - web*, pro každý pohyb zásob (příliv nebo odliv) systém vypočítá a udržuje náklady na zásoby každého produktu na úrovni lokality. Pohyby zásob na nižších úrovních, například na úrovni skladu, proto neovlivňují hodnotu zásob. (Příkladem převodu na úrovni skladu je převod zboží mezi dvěma sklady na jednom místě.) Podobně nemůžete zobrazit náklady na inventář na nižší úrovni, například na úrovni skladu.

- **Zásada základu vstupního měření** - Vyberte zásadu základu vstupního měření. Tyto zásady určují náklady, které by měly plynout na účet zásob, a náklady, které by měly být účtovány. Následující možnosti jsou relevantní pro obchodní společnosti:

    - **Normální historický** - Všechny nákladové komponenty plynou do účtu zásob.
    - **Standard** - Standardní nákladové toky na účty zásob a rozdíl mezi aplikovanou cenou a skutečnými náklady se účtuje na účty odchylek. Chcete-li vytvořit *Standardní* zásadu základu vstupního měření, musíte nejprve vytvořit ceník, kde zásada může vyhledat standardní cenu položky.
    - **Ceníky** - Globální účetnictví zásob podporuje načítání cen zboží od více právnických osob. Můžete definovat ceník, který bude používat zásada základu vstupního měření. Tímto způsobem bude systém vědět, kde hledat cenu položky. Chcete-li nastavit ceníky, postupujte následujícím způsobem:

        1. Do pole **Název** zadejte název.
        1. Zadejte popis do pole **Popis**.
        1. V poli **Typ kalkulace** vyberte typ výpočtu nákladů (*Standardní náklady* nebo *Plánované náklady*).
        1. V poli **Typ ceny** vyberte typ ceny (*Náklady*, *Nákup* nebo *Prodejní cena*).
        1. Přidat nákladové verze.
        1. V podokně akcí vyberte **Cenu** k ověření cen zboží v ceníku.

- **Zásady převzetí nákladových toků** - Vyberte zásadu převzetí toku nákladů. Tyto zásady určují, jak jsou náklady odstraněny z inventáře a vykazovány jako náklady prodaného zboží. K dispozici jsou následující předdefinované možnosti:

    - Průměr
    - Specifické - dávka

    > [!NOTE]
    > Globální účetnictví zásob je věčný inventarizační systém. Proto systém sleduje hodnotu inventáře na základě transakce po transakci.

- **Zásady nákladových prvků** - Můžete definovat zásady nákladových prvků a propojit je s tímto polem. *Nákladový prvek* je cena zdroje, který je spotřebován událostí. Ke sledování a kategorizaci nákladů můžete použít nákladové prvky. Chcete-li vytvořit zásady nákladových prvků, zadejte informace na následujících místech:

    - Pole **Název**
    - Pole **Popis**
    - Seznam **prvků nákladů**
    - Mřížka **Pravidla**

    Pokud nechcete dále rozpisovat hodnotu inventáře, musíte stále vytvořit seznam nákladových prvků, který má jeden nákladový prvek. Poté musíte vytvořit zásadu nákladových prvků, která mapuje všechny relevantní typy měření (nákladové komponenty) na daný nákladový prvek.

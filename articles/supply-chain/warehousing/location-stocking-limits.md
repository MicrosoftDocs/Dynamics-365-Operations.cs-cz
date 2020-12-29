---
title: Limity pro místo uskladnění
description: Toto téma popisuje funkčnost limitů pro místo uskladnění.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 208662f38b06b1f230bdde5247946a9fefd57cea
ms.sourcegitcommit: d2dea9ce480f35d0c0b10615c18862695e107d55
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/23/2020
ms.locfileid: "4607272"
---
# <a name="location-stocking-limits"></a>Limity pro místo uskladnění

[!include [banner](../includes/banner.md)]

Můžete použít stránku **Limity pro místo uskladnění** (**Řízení skladu \> Nastavení \> Sklad \> Limity pro místo uskladnění**) ke kontrole kapacity vytížení v místech uskladnění, aniž byste museli používat pokročilejší procesy pro objemové výpočty fyzických produktů.

Účelem limitů pro místo uskladnění je vyhodnotit maximální množství, které může skladové místo obsahovat. Tuto funkci můžete nastavit na kterékoli ze tří úrovní, z nichž každá má svou vlastní kartu na stránce **Limity pro místo uskladnění**:

- Produkty
- Varianty produktu
- Typy kontejneru

Pro každou úroveň můžete definovat různé hodnoty polí. Systém poté vyhodnotí kapacitu konkrétního skladového místa na základě hodnot **Množství** a **Jednotka** pro každý řádek. Nejprve vybere nejpodrobnější odpovídající záznam. Například řádek, který má hodnotu v poli **ID profilu skladového místa**, bude vyhodnocen před řádkem, který má hodnotu pouze v poli **Sklad**. Zbývající kapacita bude rovněž hodnocena na základě hodnoty **Množství** pro použitý záznam limitu pro místo uskladnění.

V sekci **Produkty** stránky můžete definovat následující hodnoty polí pro hledání limitů pro místo uskladnění:

- Sklad
- ID profilu skladového místa
- Skladové místo
- ID kategorie velikosti balení
- Č. položky
- Jednotka

> [!NOTE]
> Nemusíte definovat hodnotu **Jednotka** pro každý záznam limitu pro místo uskladnění. Výpočty kapacity místa budou založeny na množství jednotek zásob. Pokud není pro použitou hodnotu definován žádný převod jednotek, bude přeskočen záznam limitu pro místo uskladnění, jako by pro něj byla definována jiná hodnota **Číslo položky**.

## <a name="example--purchase-order-receiving"></a>Příklad - Přijetí nákupní objednávky

Tento příklad je založen na čisté ukázkové sadě dat *USMF*, kde jsou na kartě **Varianty produktu** stránky **Limity pro místo uskladnění** nastaveny následující hodnoty.

| Sklad | ID profilu skladového místa | Č. položky | Velikost | Množství | Jednotka |
|-----------|---------------------|-------------|------|----------|------|
| 24        | FLOOR               | D0013       | mil.    | 300      | Ea   |
| 24        | FLOOR               | D0013       | L    | 240      | Ea   |
| 24        | FLOOR               | D0013       | S    | 360      | Ea   |

Pro produkty jsou nastaveny různé varianty produktu měrných jednotek. Tyto varianty jsou v souladu s limity pro místo uskladnění pro tři palety (PL):

- **Velikost M:** 1 PL = 100 každá (Ea)
- **Velikost L:** 1 PL = 80 Ea
- **Velikost S:** 1 PL = 120 Ea

Proto každé místo, kde je hodnota **ID profilu skladového místa** nastavena na *FLOOR* může nést *3* *PL* čísla položky *D0013*.

### <a name="prepare-for-the-example"></a>Připravte se na příklad

V tomto příkladu spustíte tok přijímání nákupní objednávky pro dva řádky. Nejprve však musíte aktualizovat ukázková data následujícím způsobem, aby bylo zajištěno, že umístění umožňuje kombinované položky, pouze prázdná umístění *FL-002* přes *FL-004* se použijí a neexistuje žádná otevřená příchozí práce.

1. Pro umístění *FL-001* změňte hodnotu pole **Profil umístění** z *FLOOR* na *FLOOR-05*.
1. Pro profil místa *FLOOR* nastavte možnost **Povolit smíšené položky** na *Ano*.
1. Vytvořte nákupní objednávku, který má následující dva řádky:

    | Sklad | Č. položky | Velikost | Množství | Jednotka |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | S    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Zpracování příkladu

Nejprve obdržíte množství *4* jednotky *PL* ve velikosti *S* a zkontrolujte umístění řádku vložení pro vytvořenou práci. Pak obdržíte množství *4* jednotky *PL* ve velikosti *L* a zkontrolujte umístění řádku vložení pro vytvořenou práci.

1. Ve skladovací aplikaci se přihlaste pomocí čísla *24* ID uživatele a *1* jako heslo.
1. Vyberte **Příchozí** \> **Příjem nákupu**..
1. Přijměte *4* *PL* čísla položky *D0013* ve velikosti *S*.
1. Zkontrolujte vytvořenou práci založení. Měl by se vám zobrazit následující výsledek:

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Přijměte *4* *PL* čísla položky *D0013* ve velikosti *L*.
1. Zkontrolujte vytvořenou práci založení. Měl by se vám zobrazit následující výsledek:

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

Na základě výsledků můžete dojít k závěru, že se systému nepodařilo přidělit správná místa založení. V opačném případě, proč systém přidal pouze *1* *PL* velikosti *L* na místo *FL-003* v posledním kroku, a nikoliv *2* *PL*? Proč tam není celkem *3* *PL* pro založení na toto místo?

Chcete-li vysvětlit toto zjevné selhání, musíte porozumět kritériím výběru limitů pro místo uskladnění. Systém vybere nejpodrobnější odpovídající záznam. V tomto příkladu je nejpodrobnějším odpovídajícím záznamem řádek, kde hodnota **Velikost** je *L*, **Množství** je *240* a **Jednotka** je *Ea*. Protože již máte otevřenou práci z předchozího přijetí množství *120* *Ea* velikosti *S*, zbývající kapacita se vypočítá jako *240* – *120* = *120* *Ea*. Zbývající kapacita tedy může být pouze *1* *PL* of *80* *Ea*.

> [!NOTE]
> Limity pro místo uskladnění nemůžete použít například ke kontrole doplnění položek, které mají ve stejném umístění různá množství. V takovém případě použijte *šablonu doplnění*.

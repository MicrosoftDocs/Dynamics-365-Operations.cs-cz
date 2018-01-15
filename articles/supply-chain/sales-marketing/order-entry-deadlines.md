---
title: "Konečné termíny zadání objednávek"
description: "Tento článek poskytuje informace o konečných termínech objednávky. Konečný termín objednávky je časový interval přerušení, který určuje, zda je objednávka odběratele zpracována (a plněna), jako by byla přijata aktuálního dne nebo následujícího dne."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 31308e64d4871a4d09540df16fdcd02cc83bd0be
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="order-entry-deadlines"></a>Konečné termíny zadání objednávek

[!include[banner](../includes/banner.md)]


Tento článek poskytuje informace o konečných termínech objednávky. Konečný termín objednávky je časový interval přerušení, který určuje, zda je objednávka odběratele zpracována (a plněna), jako by byla přijata aktuálního dne nebo následujícího dne.

V mnoha společnostech je pouze prodejní objednávka přijatá do určitého termínu daného dne zpracována jako objednávka přijatá toho dne. Všechny objednávky, které byly přijaty po uplynutí této doby, jsou považovány za přijaté v následující pracovní den. Tento čas přerušení pro objednávky se nazývá konečný termín zadání objednávky.  

Konečné termíny zadání objednávky se používají jako vstup pro příslib objednávek. Proto pomáhají spravovat očekávání odběratelů ohledně dodávky objednávky. Odběratele mohou například vidět, že pokud u vás podají objednávky před určeným časem, zajistíte expedici zboží ve stejný den. Pokud však tento termín zmeškají, mohou očekávat dodávky pouze na následující pracovní den. Konečné termíny zadání objednávek nastavujete na základě funkce skladu a expedičních plánů dopravce.  

Na stránce **Konečné termíny zadání objednávek** jsou uvedeny termíny zadání objednávky pro všechny dny v týdnu. Všechny objednávky, které byly přijaty po uplynutí této doby, jsou považovány za přijaté v následující den. Výchozí nastavení času těchto termínů je 23:59, jednu minutu před půlnocí na konci příslušného dne. Výchozí časy lze změnit tak, aby odpovídaly skutečným časům expedice nebo příjmu.  

Konečné termíny podání objednávky můžete definovat pro konkrétní skupinu odběratelů. Můžete například chtít, aby určitá skupina zákazníků měla termíny podání objednávky, které jsou novější, než ty od jiných odběratelů. V takovém případě nejprve definujete skupiny pro konečné termíny zadání objednávek na stránce **Skupiny konečných termínů zadání objednávek**. Potom přiřadíte skupiny odběratelům na stránce **Odběratelé**.  

Jestliže má vaše společnost pobočky na více místech, můžete nastavit termíny zadání objednávky pro každou pobočku. Jestliže jsou pobočky v různých časových pásmech, je termín zadání objednávky nastaven v časovém pásmu pobočky. Avšak při práci s prodejními objednávkami a prodejními nabídkami je termín zadání objednávky převeden na vaše časové pásmo na stránce **Dostupná data expedice a příjmu**.  

Na stránce **Aktivovat kombinace konečných termínů zadání objednávek** lze definovat kombinace konečných termínů pracovišť a zadání objednávky, které jsou povoleny.

## <a name="example-order-entry-deadline"></a>Příklad: Konečný termín zadání objednávky
Konečný termín pro zadání objednávky v úterý byl nastaven na 16:00. K určitému úterý v 17:00 se pokusíte nastavit aktuální datum jako datum dodání. (Pro tento příklad neexistuje žádná doba realizace.)Pokud označíte pole **Řízení data dodání**, zobrazí se varovná zpráva oznamující, že datum není platné. Toto upozornění se zobrazí na stránce **Dostupná data expedice a příjmu**, kde můžete vybrat alternativní data.

## <a name="example-different-order-entry-deadlines-per-site"></a>Příklad: Různé termíny zadání objednávky pro různé pobočky
Vaši společnost tvoří dvě pobočky. Pobočky se nachází v různých časových pásmech, jak je uvedeno v následující tabulce.

| Pobočka A                      | Pobočka B                      |
|-----------------------------|-----------------------------|
| Kalifornie                  | Florida                     |
| Tichomořský standardní čas (PST – Pacific Standard Time) | Východní standardní čas (EST – Eastern Standard Time) |

Pobočka A a B má definovány následující termíny zadání objednávky.

| Den v týdnu             | A: Konečné termíny zadání objednávek (PST) | B Konečné termíny zadání objednávek (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Pondělí                      | 13:00                          | 14:00                          |
| Úterý                     | 13:00                          | 14:00                          |
| Středa                   | 13:00                          | 14:00                          |
| Čtvrtek                    | 13:00                          | 14:00                          |
| Pátek                      | 13:00                          | 14:00                          |

Zpracováváte objednávku v Utahu, kde je časové pásmo Horský standardní čas (MST – Mountain Standard Time). To znamená, že pokud zadáte objednávky pro pobočku A před 14:00 MST a podáte objednávky pro pobočku B před 12:00 MST, stihnete pro obě pobočky zadat objednávku v termínu.  

Následující tabulka obsahuje konečné termíny zadání objednávky pro pobočku A a B převedené na čas MST.

| Pobočka A: (PST)         | Pobočka B: (MST)        | Pobočka B: EST           | Pobočka B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 14:00                 | 12:00              |

**Poznámka:** Pokud se používá úprava na letní čas, jsou termíny zadání objednávky upraveny odpovídajícím způsobem.

## <a name="example-same-order-entry-deadline-per-site"></a>Příklad: Stejný termín zadání objednávky pro různé pobočky
Vaši společnost tvoří dvě pobočky. Pobočky se nachází v různých časových pásmech, jak je uvedeno v následující tabulce.

| Pobočka A                      | Pobočka B                      |
|-----------------------------|-----------------------------|
| Kalifornie                  | Florida                     |
| Tichomořský standardní čas (PST – Pacific Standard Time) | Východní standardní čas (EST – Eastern Standard Time) |

Pobočka A a B má definovány následující termíny zadání objednávky.

| Den v týdnu | PST a EST |
|-----------------|-------------|
| Pondělí          | 13:00       |
| Úterý         | 13:00       |
| Středa       | 13:00       |
| Čtvrtek        | 13:00       |
| Pátek          | 13:00       |

Zpracováváte objednávku v Utahu, kde je časové pásmo Horský standardní čas (MST – Mountain Standard Time). To znamená, že pokud zadáte objednávky pro pobočku A před 14:00 MST a podáte objednávky pro pobočku B před 11:00 MST, stihnete pro obě pobočky zadat objednávku v termínu. 

Následující tabulka obsahuje konečné termíny zadání objednávky pro pobočku A a B převedené na čas MST.

| Pobočka A: (PST)         | Pobočka A: (MST)        | Pobočka B: EST           | Pobočka B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 13:00                 | 11:00              |

**Poznámka:** Pokud se používá úprava na letní čas, jsou termíny zadání objednávky upraveny odpovídajícím způsobem.

<a name="see-also"></a>Viz také
--------

[Plány dodávek](delivery-schedules.md)





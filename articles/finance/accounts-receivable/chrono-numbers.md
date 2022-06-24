---
title: Chronologické číslování dokumentů a dokladů
description: Tento článek vysvětluje, jak nastavit a používat chronologická čísla pro příslušné dokumenty a související doklady.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6baf307406982e8f72acc0d02f047dbc7c63a5ed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876376"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Chronologické číslování dokumentů a dokladů

[!include [banner](../includes/banner.md)]


V některých zemích existuje zákonný požadavek na číslování dokumentů a souvisejících dokladů v chronologickém pořadí. Chronologie musí být podporována obdobími. Všechna čísla, která patří do dřívějších období, musí být menší než čísla, která patří do pozdějších období. Pro splnění tohoto požadavku byla implementována funkce chronologického číslování. Tento článek vysvětluje, jak konfigurovat a používat chronologická čísla pro příslušné dokumenty a související doklady.

## <a name="prerequisites"></a>Předpoklady

V pracovním prostoru Správa funkcí zapněte funkci **Chronologické číslování**: Další informace naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Konfigurace chronologického číslování

Chronologické číslování má vliv na následující dokumenty.

**Pohledávky**
- Faktura zákazníka
- Doklad faktury odběratele
- Prodejní dobropis
- Doklad prodejního dobropisu
- Volné faktury
- Doklad volné faktury
- Dobropis s volným textem
- Úplný text dobropisu dokladu
- Dodací list
- Doklad dodacího listu
- Doklad o opravě dodacího listu
- Doklad oznámení úroků
- Doklad upomínky

**Závazky**
- Doklad faktury
- Doklad dobropisu
- Doklad příjemky produktu

**Správa projektu**
- Faktura
- Doklad faktury
- Dobropis
- Doklad dobropisu 

### <a name="define-number-sequences"></a>Definice číselných řad

Chcete-li definovat číselné řady, přejděte na **Správa organizace** > **Číselné řady** > **Číselné řady**. Můžete definovat tolik číselných sekvencí, kolik je požadováno pro pokrytí ovlivněných období pro požadované dokumenty. 

Zadejte společnost pro každou číselnou řadu. Segmenty číselných sekvencí musí být definovány tak, aby tvořily chronologické pořadí pro období. Názvy segmentů mohou například obsahovat speciální předponu, která identifikuje konkrétní období.

![Nastavení číselných řad.](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Konfigurace skupin číselných řad

Chcete-li konfigurovat skupiny číselných řad, přejděte na **Pohledávky** > **Nastavení** > **Parametry pohledávek**. Na kartě **Číselné řady** definujte tolik skupin číselných sekvencí, kolik je potřeba k pokrytí ovlivněných období. 

Pro každou skupinu v části **Odkaz** vyberte jeden z podporovaných odkazů na dokumenty a v části **Kód číselné řady** zadejte číselnou řadu, která byla dříve vytvořena pro příslušné období.

![Nastavení skupiny číselných řad.](media/chrono-num-sequence-group.jpg)

Podobně nakonfigurujte skupiny číselných řad v modulech **Pohledávky** a **Řízení projektů a účetnictví**.

### <a name="configure-number-sequence-groups-chronology"></a>Konfigurace chronologie skupin číselných řad

Chcete-li nakonfigurovat chronologii skupin číselných řad, přejděte na **Správa organizace** > **Číselné řady** > **Skupiny chronologických číselných řad**. Definujte podmínky použitelnosti pro skupiny číselných sekvencí.

![Nastavení chronologických čísel.](media/chrono-num-sequence-group-period.jpg)

| Pole            | popis                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Účinné:  | Datum zahájení použitelnosti skupiny číselných řad. |
| Vypršení platnosti      | Koncové datum použitelnosti skupiny číselných řad. Pokud není použito žádné datum ukončení, vyberte **Nikdy**. |
| Skupina číselné řady | Skupina číselných řad, která bude použita ke generování čísel dokumentů během období. |
| Původní skupina číselných řad | Tento kód skupiny číselných sekvencí se používá pro další filtrování pro případy, kdy dokumenty již mají přiřazenou konkrétní *trvalou* skupinu číselných řad. Prázdná hodnota se považuje za konkrétní hodnotu. Pokud potřebujete ignorovat předběžně přiřazenou skupinu, použijte **Výchozí** možnost pro toto nastavení. |
| Výchozí | Pokud je zapnuto, systém ignoruje předběžně přiřazenou skupinu čísel dokumentů a pro analýzu použitelnosti používá pouze počáteční a koncová data období. Pokud je vypnuto, systém používá pro výběr celou kombinaci **Platnost** + **Vypršení** + **Původní skupina číselných řad**. |

## <a name="document-posting"></a>Zaúčtování dokumentu
Když zaúčtujete dokument, je dokumentu přiřazena příslušná skupina číselných řad na základě data zaúčtování dokumentu a poté je použita ke generování čísla dokumentu na základě zjištěné číselné řady. Systém poskytuje zprávu týkající se přiřazení skupiny číselných řad.

![Číslo dokumentu](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> V některých zemích již existuje specifická logika pro číslování dokumentů. V takovém případě logika konkrétní země přepíše funkci **Chronologické číslování**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

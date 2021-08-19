---
title: Správa technických změn – časté otázky
description: V tomto tématu jsou odpovědi na časté otázky týkající se funkce správy technických změn.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ba489358ef2d74e816186f29956aea5538a2432825c7d949e7c9cc23d947b997
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714371"
---
# <a name="engineering-change-management-faq"></a>Správa technických změn – časté otázky

[!include [banner](../includes/banner.md)]

V tomto tématu jsou odpovědi na časté otázky týkající se funkce správy technických změn.

## <a name="should-i-track-the-version-in-transactions"></a>Mám sledovat verze v transakcích?

Když vytvoříte kategorii technické změny, stránka **Podrobnosti kategorie technické změny** poskytuje možnost s názvem **Sledovat verze v transakcích**. Co je toto nastavení a co dělá?

- Pokud nastavíte možnost **Sledovat verze v transakcích** na *Ano*, pole **Skupina dimenzí** bude filtrováno tak, aby zobrazovalo pouze skupiny dimenzí, kde je verze aktivní dimenzí.
- Pokud nastavíte možnost **Sledovat verze v transakcích** na *Ne*, pole **Skupina dimenzí** bude filtrováno tak, aby zobrazovalo pouze skupiny dimenzí, kde dimenze verze **není** aktivní dimenze.

### <a name="if-you-track-the-version-in-transactions"></a>Když sledujete verze v transakcích

U technických kategorií, kde jste vybrali skupinu dimenzí, kde je verze aktivní dimenzí, budete sledovat verze v transakcích pro produkty v této kategorii. V tomto případě bude technický produkt základní produkt a každá verze produktu bude variantou produktu, která používá dimenzi verze. Spolu s dimenzí verze lze použít i jiné dimenze.

V tomto případě bude každá technická verze považována za variantu ve všech procesech. Pokud tedy máte v transakci konkrétní variantu (abyste mohli určit, která varianta byla prodána nebo zakoupena), musíte pro každou verzi spravovat zásoby, hlavní plánování naplánuje dodávku pro každou verzi atd. Pokud odstraníte verzi z trhu, musíte ručně upravit její datum účinnosti od a do dne tak, aby odráželo změnu. Musíte také spravovat zásoby, abyste zajistili, že ve skladech nemáte nepoužívané verze položek.

Ačkoli tato možnost vyžaduje více úsilí pro správu, doporučujeme ji, pokud požadujete vysokou sledovatelnost konkrétních verzí, které se používají v každé transakci.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Když nesledujete verze v transakcích

U technických kategorií, kde jste vybrali skupinu dimenzí, kde verze **není** aktivní dimenzí, **nebudete** sledovat verze v transakcích pro produkty v této kategorii. V tomto případě, pokud nepoužíváte žádnou jinou dimenzi, bude technický produkt jedinečný produkt. Produkt bude stále mít verze a můžete spravovat informace o konkrétních verzích (například jejich kusovník \[BOM] a trasu), ale nebudete moci vysledovat, která konkrétní verze byla použita v každé transakci. Datum účinnosti od a do označuje platnost každé verze.

Tato možnost je mnohem snazší spravovat, protože pokud chcete přejít z jedné verze na druhou, stačí provést požadované změny v pořadí změn a poté aktualizovat data účinnosti od a do v technické verzi. Výrobní procesy poté vyzvednou požadovaný kusovník a trasu pro produkt (a jeho konkrétní verzi).

Většina organizací volí tuto možnost, protože poskytuje správu verzí a změn, ale nepřidává další režii sledování verze v každé transakci, v zásobách a během hlavního plánování.

## <a name="which-fields-are-copied-from-the-released-item-template"></a>Která pole se zkopírují z vydané šablony položky?

Když technická společnost vytvoří technický produkt, vytvoří se tento produkt jako uvolněný produkt v technické společnosti. Vydaný produkt, který je vytvořen, je založen na vybrané *šabloně vydané položky*. (Šablona vydané položky je sama o sobě existujícím vydaným produktem.) Šablona vydané položky se také používá, když je produkt vydán provozní společnosti. V každém případě šablona vydané položky definuje většinu hodnot polí pro vydaný produkt a tyto hodnoty pocházejí z přidružené stránky **Údaje o vydaném produktu**.

Následující tabulky ukazují pole, která se zkopírují během těchto procesů.

| Pevná záložka | Pole, která se kopírují při vytváření produktu v technické společnosti | Pole, která se při vydání zkopírují do provozní společnosti |
|---|---|---|
| **Obecný** | Všechna pole v části **Správa** | Stejná pole, která se kopírují pro technickou společnost |
| **Nákup** | Všechna pole | Všechna pole kromě **Jednotka** |
| **Prodej** | Všechna pole v následujících částech: **Prodejní objednávka**, **Správa**, **Zdanění**, **Aktualizace ceny**, **Základní prodejní cena**, **Poplatky**, **Slevy** a **Alternativní produkt** | Všechna stejná pole, která se kopírují pro technickou společnost, kromě **Jednotka** |
| **Zahraniční obchod** | Všechna pole | Všechna pole |
| **Spravovat sklad** | Všechna pole a sekce *kromě* **Fyzické rozměry** a **Skutečná hmotnost** | Všechna stejná pole, která se kopírují pro technickou společnost, kromě **Jednotka** |
| **Technik**, **Plán**, **Spravovat náklady**, **Spravovat projekty**, **Finanční dimenze** a **Sklad** | Všechna pole | Všechna pole kromě **Jednotka kusovníku** |
| **Varianty produktu** | Všechna pole v části **Výchozí varianta produktu** | Stejná pole, která se kopírují pro technickou společnost |

Kromě polí, která jsou uvedena v předchozí tabulce, se z šablony vydané položky zkopírují všechna výchozí nastavení objednávek, a to jak při vytvoření produktu v v technické společnosti, tak při jeho vydání provozní společnosti. (Chcete-li zobrazit výchozí nastavení objednávky pro šablonu vydané položky, otevřete příslušnou stránku **Údaje o vydaném produktu** a poté na panelu akcí na kartě **Správa zásob** vyberte **Výchozí nastavení objednávky**.)

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Mám vytvořit samostatnou právnickou osobu pro technické produkty, nebo použít existující právnickou osobu?

Vaše obchodní požadavky určují, zda byste měli vytvořit nový právní subjekt pro technické produkty.

Vytvořením samostatné technické společnosti můžete zachovat samostatná technická data a poté přidat úpravy, které jsou vyžadovány pro vaše místní provozní společnosti. Tímto způsobem můžete dosáhnout následujících cílů:

- Udržování samostatné entity, kde se vytvářejí a spravují technické produkty.
- Zabránění tomu, aby se technické produkty zobrazovaly společně se zbytkem vašich vydaných produktů, dokud nebudou připraveny a vydány.
- Jasné rozlišení dat, která jsou diktována technickými a místními daty.

Na druhou stranu byste pravděpodobně měli použít stávající právnickou osobu jako technickou společnost, pokud se na vás vztahují následující podmínky:

- Ve svém systému máte pouze jednu právnickou osobu nebo nevyžadujete jasné oddělení mezi produkty, které jsou vyvíjeny.
- Nechcete duplikovat některá data, například skupiny prostředků, prostředky, operace a (možná) pracoviště.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Jaká je nomenklatura pro technické verze a varianty?

Nomenklatura pro technické produkty a varianty produktů funguje následujícím způsobem:

- Pro technický produkt (tj. jedinečný produkt, pokud se nepoužívají žádné dimenze, nebo hlavní produkt, pokud se používá jakákoli dimenze) je v kategorii technického produktu definována nomenklatura pravidla počtu. Zde máte možnost použít číselnou sekvenci, textové konstanty a názvy a hodnoty atributů.
- Pro každou variantu technického produktu (je-li technický produkt hlavní produkt, jsou varianty nastaveny v kategorii technického produktu, kde určíte skupinu dimenzí), je ve skupině dimenzí definována nomenklatura číselného pravidla pro každou variantu. V tomto případě můžete použít ID produktu hlavního produktu a hodnoty a názvy dimenzí.

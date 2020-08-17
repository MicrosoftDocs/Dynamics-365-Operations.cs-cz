---
title: Nakonfigurujte sekvence čísel pro toky skladu
description: Toto téma poskytuje přehled funkcí, které poskytují rozšíření číselných sekvencí pro ID poznávacích značek, ID popisků vlny, ID kontejnerů a ID přepravních dokladů.
author: GarmMSFT
manager: tfehr
ms.date: 06/10/2020
ms.topic: configure-number-sequence-extensions
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSNumberSequenceExtension
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 2f4506d2c1808198d4b10e50f4635bcc21d934e1
ms.sourcegitcommit: 0f877ee4b53cfb002b179a53a67c4f9adae354bf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/30/2020
ms.locfileid: "3640392"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Nakonfigurujte sekvence čísel pro toky skladu

[!include [banner](../includes/banner.md)]

Funkce *Rozšíření číselných sekvencí* přidá novou konfigurační stránku pro nastavení číselných sekvencí. Umožňuje flexibilní konfiguraci identifikátorů regulovaných GS1, včetně předpon GS1 a kontrolních číslic (modulo 10), a vynucuje omezení délky existujících číselných sekvencí.

Standardní segmenty sekvencí čísel nejsou vhodné pro implementaci GS1, protože se nevypočítává žádná kontrolní číslice a předponu GS1 společnosti je nutné aktualizovat ručně.

Ta přidává následující funkce:

- ID přepravního dokladu (BOL) lze vygenerovat předem.
- Pro čísla sériových přepravních kontejnerů (SSCC) lze vygenerovat jedinečnou sekvenci čísel.
- Pro čísla BOL a SSCC lze vytvořit číselné sekvence kompatibilní s GS1. Tato funkce přidává podporu pro identifikační čísla poznávacích značek, ID kontejnerů, ID popisků vlny a ID BOL.
- Konfigurace identifikačních čísel poznávacích značek je flexibilní. Například můžete zahrnout nebo vyloučit identifikátory aplikace (AI), jako jsou například počáteční nuly (00).

Tato funkce zefektivňuje podporu označování kartonů a úpravu nových čísel generovaných systémem.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Zapněte funkci Rozšíření posloupnosti čísel

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Rozšíření posloupnosti čísel*

## <a name="set-up-the-feature"></a>Nastavení funkce

Chcete-li v systému nastavit rozšíření číselných sekvencí, postupujte takto.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na kartě **Všeobecné** v poli **Předpona společnosti GS1** zadejte předponu GS1 vaší společnosti. Tato hodnota ovlivní všechny sekvence čísel, kde je předpona GS1 zahrnuta jako segment.
1. Pokud chcete generovat čísla BOL pro popisky vlny, na kartě **Sestavy** zaškrtněte **Při tisku štítků s vlnou vygenerujte číslo BOL**.

    > [!NOTE]
    > Toto zaškrtávací políčko je k dispozici, pouze pokud je funkce pro [tisk štítků vlny](configure-wave-label-printing.md) zapnuta.

1. Přčejděte na **Správa skladu** \> **Založit** \> **Rozšíření číselných sekvencí**
1. V podokně akcí vyberte **Vytvořit výchozí nastavení**. Vytvoří se sekvence čísel BOL kompatibilní s GS1 a tři typy číselných sekvencí SSCC. Všechny tyto číselné sekvence berou v úvahu délku předpony GS1 vaší společnosti.

    Další informace o tom, jak přizpůsobit tyto výchozí číselné sekvence a / nebo přidat nové sekvence, naleznete v další části. Můžete také odstranit kteroukoli z těchto sekvencí, pokud je nepotřebujete.

1. Přejděte zpět na **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na kartě **Číselné sekvence** vyberte příslušné rozšíření sekvence čísel, která se použije pro generování čísel pro vaše poznávací značky, ID popisků vlny, ID kontejnerů (v tomto případě vyberte příslušnou sekvenci **Číslo SSCC-18**) a / nebo BOL ID (v tomto případě vyberte sekvenci **BOL**). Ve výchozím nastavení jsou rozšíření číselných sekvencí podporována pouze pro tyto čtyři typy ID.

Při příštím vygenerování nového čísla pro jednu z těchto číselných sekvencí bude použita nová logika.

> [!NOTE]
> Pokud nevyberete rozšíření číselné sekvence pro ID poznávací značky, budou použita aktuální pravidla pro generování ID poznávací značky. Jinak bude použita zvolená posloupnost čísel. Ostatní ID budou používat prostou posloupnost čísel, dokud na ně nepoužijete rozšíření posloupnosti čísel.

## <a name="create-and-edit-number-sequences"></a>Vytvářejte a upravujte sekvence čísel

V předchozí části jste vygenerovali výchozí sadu číselných sekvencí. Tato část vysvětluje, jak je definována každá posloupnost čísel. Vysvětluje také, jak vytvořit vlastní sekvence a jak upravit výchozí nebo vlastní sekvence.

Chcete-li vytvořit a upravit posloupnosti čísel, postupujte takto.

1. Přejděte na **Správa skladu** \> **Založit** \> **Rozšíření číselných sekvencí**.
1. V podokně akcí zvolte **Nový**.
1. V poli **Rozšíření sekvence čísel** zadejte název nové sekvence. Zadejte popis do pole **Popis**.
1. Na pevné záložce **Segmenty** pomocí tlačítek na panelu nástrojů sestavte formát číslování přidáním, odstraněním a uspořádáním segmentů. V poli **Segment** pro každý řádek přiřaďte typ segmentu k definování účelu a obsahu tohoto segmentu. Následující tabulka popisuje typy segmentů, které jsou k dispozici.

    | Typ segmentu | popis |
    |---|---|
    | Konstanta | Tento typ segmentu přidá stejný konstantní text pro každé vygenerované číslo v sekvenci. V poli **Hodnota** zadejte požadovaný text. Pole **Délka** je automaticky aktualizováno na délku textu, který jste zadali do pole **Hodnota**. |
    | Číselná řada | V poli **Hodnota** zadejte číselný znak (*\#*) pro každý znak, který by měl být zobrazen ve vygenerované sekvenci. Samotná posloupnost čísel může generovat delší čísla, ale zobrazí se pouze ty nejprávnější znaky. Pole **Délka** je automaticky aktualizováno na počet číselných znaků, který jste zadali do pole **Hodnota**.<p>Chcete-li splnit požadavky GS1 pro čísla SSCC-18, ujistěte se, že délka tohoto segmentu je 16 minus délka předpony GS1.</p> |
    | Předpona GS1 | Tento typ segmentu přidá hodnotu nastavenou v poli **Předpona společnosti GS1** na stránce **Parametry správy skladu**. Pole **Hodnota** zobrazuje hodnotu, která je nastavena na stránce **Parametry správy skladu** a pole **Délka** zobrazuje počet znaků v hodnotě. Pole **Hodnota** i **Délka** jsou jen pro čtení. |
    | Aplikační identifikátor | V poli **Hodnota** zadejte identifikátor aplikace, jak je stanoveno v příslušných zásadách GS1 pro tento typ číselné sekvence. Například zadejte *00* pro SSCC nebo *420* pro BOL. Pole **Délka** je automaticky aktualizováno na délku identifikátoru, který jste zadali do pole **Hodnota**. |
    | Typ balení | U položek, které lze jasně identifikovat, přidá tento typ segmentu hodnotu pole z příslušné skupiny sekvencí jednotek (ze stránky **Skupiny sekvencí jednotek**). (Toto chování odpovídá existující logice pro ID poznávacích značek.) U poznávacích značek, které zahrnují více jednotek uchovávání zásob (SKU), tento typ segmentu přidá *0* (nula) ve výchozím nastavení. Pro tento typ segmentu je pole **Hodnota** je vždy nastaveno na *P* a pole **Délka** je vždy nastaveno na *1*.|
    | Kontrolní číslice | Tento typ segmentu přidá kontrolní číslici, což je výpočet modulo 10. (Toto chování odpovídá existující logice pro ID poznávacích značek.) Pro tento typ segmentu je pole **Hodnota** vždy nastaveno na stříšku (*^*) a pole **Délka** na *1*. |

1. Chcete-li zobrazit příklad konečného formátu čísla, prohlédněte si pole **Formát** ve spodní části pevné záložky **Segmenty**.

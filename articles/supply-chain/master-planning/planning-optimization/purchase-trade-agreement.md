---
title: Hlavní plánování s obchodními smlouvami nákupu
description: Tento článek popisuje, jak může hlavní plánování najít dodavatele a / nebo doby realizace pro plánovanou objednávku na základě nejlepší ceny nebo doby realizace, které se nacházejí ve smlouvách o nákupu.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c36827738b13d5ca71da910d32e8877c1a408f62
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740978"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Hlavní plánování s obchodními smlouvami nákupu

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak může hlavní plánování najít dodavatele a / nebo doba realizace pro plánovanou objednávku na základě nejlepší ceny nebo doby realizace, které se nacházejí ve všech smlouvách o nákupu specifikovaných pro daný produkt.

## <a name="turn-the-purchase-trade-agreements-for-planning-optimization-feature-on-or-off"></a>Zapnutí nebo vypnutí funkce nákupu obchodních smluv pro plánování optimalizace

Pokud chcete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.29, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Obchodní nákupní smlouvy pro optimalizaci plánování* v pracovním prostoru [Správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Příprava systému na vyhodnocení obchodních dohod během hlavního plánování

Chcete-li nakonfigurovat systém tak, aby používal hlavní plánování, která vyhodnocuje nákupní obchodní smlouvy, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Parametry hlavního plánování**. Na kartě **Plánované objednávky** v části **Dodavatel** nastavte následující hodnoty:

    - **Najít obchodní smlouvu** - Nastavte tuto možnost na **Ano**, chcete-li zahrnout obchodní smlouvy do územního plánování.
    - **Vyhledávací kritérium** - Vyberte faktor, který chcete upřednostnit pro každou nákupní obchodní smlouvu: **Minimální doba realizace** nebo **Nejnižší jednotková cena**.

1. Přejděte na **Nákup a zajištění zdrojů \> Nastavení \> Ceny a slevy \> Aktivovat cenu / slevu** a ujistěte se, že je možnost **Dodavatel** nastavená na **Ano**.
1. Přejděte na **Správa informací o produktu \> Nastavení \> Skupiny dimenzí a variant \> Skupiny dimenzí úložiště** a vyberte skupinu dimenzí úložiště, která se vztahuje na produkty, jejichž hlavní plánování by mělo vyhodnotit nákupní obchodní smlouvy. Ujistěte se, že každá příslušná dimenze úložiště v této skupině má zaškrtnuté políčko ve sloupci **Pro nákupní ceny**. Tento krok opakujte pro každou další relevantní skupinu dimenzí úložiště.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Příprava vydaného produktu na vyhodnocení obchodních dohod během hlavního plánování

Poté, co je systém připraven, jak je popsáno v předchozí části, byste měli podle následujících kroků ověřit, že každý produkt, který chcete s touto funkcí použít, je správně nastaven.

1. přejděte na **Správa informací o produktu \> Produkty \> Vydané produkty** a otevřete cílový produkt.
1. Na pevné záložce **Nákup** se ujistěte, že v poli **Dodavatel** není přiřazen žádný dodavatel.
1. Vyberte produkt a pak v podokně akcí na kartě **Plán** ve skupině **Disponibilita** vyberte **Disponibilita položky** pro otevření stránky **Disponibilita položky** vybraného produktu. Ověřte následující nastavení:

    - Na kartě **Obecné** můžete nastavit přepisy dodavatele. Pokud chcete, aby hlavní plánování použila nákupní smlouvy k výběru dodavatele, měli byste zabránit přepsání dodavatele zrušením zaškrtnutí políčka **Použít konkrétní nastavení**.
    - Na kartě **Doba realizace** můžete nastavit přepsání doby realizace. Pokud chcete, aby hlavní plánování použilo nákupní smlouvy k výběru dob realizace, měli byste zabránit přepsání dob realizace. Zrušte zaškrtnutí políčka u všech typů doby realizace, které chcete vybrat, pomocí obchodních smluv (**Nákup**, **Výroba** a / nebo **Převod**).

1. Zavřete stránku **Disponibilita položky** pro návrat na stránku s podrobnostmi o vybraném produktu.
1. V podokně akcí na kartě **Plán** ve skupině **Prognóza** vyberte **Prognóza dodávky** k otevření stránky **Prognóza dodávky**. Ujistěte se, že žádný řádek, který je zde zobrazen, nemá hodnotu ve sloupci **Účet dodavatele**.
1. Zavřete stránku **Prognóza dodávky** pro návrat na stránku s podrobnostmi o vybraném produktu.
1. V podokně akcí na kartě **Nákup** ve skupině **Obchodní smlouvy** vyberte **Zobrazit obchodní smlouvy**. Ujistěte se, že jsou uvedeny všechny relevantní nákupní obchodní smlouvy. Také se ujistěte, že je možnost **Ignorovat dobu realizace** nastavena na **Ne** pro každou smlouvu, jejíž hlavní plánování má používat dobu realizace, která je pro tuto smlouvu zadána.
1. Vyberte produkt a pak v podokně akcí na kartě **Plán** ve skupině **Nastavení objednávky** vyberte **Výchozí nastavení objednávky** pro otevření stránky **Výchozí nastavení objednávky** vybraného produktu. Na pevné záložce **Nákupní objednávka** se podívejte na hodnotu pole **Doba realizace**. Pokud není definováni přepsání doby realizace disponibility položky, hlavní plánování použije tuto hodnotu při výběru obchodních smluv, kde je možnost **Ignorovat dobu realizace** nastavená na **Ano**. Tuto hodnotu byste proto měli upravit podle potřeby.
1. Tento postup opakujte pro každý relevantní produkt.

> [!NOTE]
> Podpora hlavního plánování pro nákupní obchodní smlouvy ve více měnách. Při hledání obchodní dohody pomocí možnosti **Nejnižší jednotková cena** zváží systém řádky nákup obchodních dohod s různými měnami za předpokladu, že byl definován směnný kurz mezi měnou linií obchodních dohod a účetní měnou právnické osoby. Jinak bude řádek obchodní dohody ignorován a během hlavního plánování uvidíte chybu. Proto hlavní plánování bude zahrnovat informace ze všech příslušných řádků dohod o nákupu a nákupu, kde lze ceny převést na účetní měnu. Je důležité si uvědomit, že pravidla zaokrouhlování nebudou při přepočtu ceny obchodní dohody zohledněna.

## <a name="examples-of-how-master-planning-finds-vendor-and-lead-times"></a>Příklady toho, jak hlavní plánování vyhledává dodavatele a doby realizace

Následující tabulka uvádí příklady, které ukazují, jak různá nastavení vydaného produktu a souvisejících nákupních obchodních smluv ovlivňují hodnoty, které jsou nalezeny pro výslednou plánovanou objednávku. Hodnoty zobrazené **tučně** ve dvou sloupcích zcela vpravo jsou hodnoty, které jsou vybrány pomocí hlavního plánování. Hodnoty uvedené **_tučně a kurzívou_** v ostatních sloupcích jsou nastavení, která vytvořila tyto výsledné hodnoty pro každý řádek.

| Vydaný produkt: dodavatel | Výchozí nastavení objednávky: doba realizace | Pokrytí položky: Přepsat dodavatele | Pokrytí položky: Přepsat dobu realizace | Obchodní smlouva: dodavatel | Obchodní smlouva: doba realizace | Obchodní smlouva: Ignorovat dobu realizace | Výsledný dodavatel | Výsledná doba realizace |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001** _ | _*_1_*_ | Ne | Ne | US003 | 3 | Ne | _ *US001** | **1** |
| US001 | 1 | ***Ano: US002** _ | _*_Ano: 2_*_ | US003 | 3 | Ne | _ *US002** | **2** |
| *(Prázdné)* | 1 | Ne | Ne | ***US003** _ | _*_3_*_ | Ne | _ *US003** | **3** |
| *(Prázdné)* | ***1** _ | Ne | Ne | _*_US003_*_ | 3 | Ano | _ *US003** | **1** |
| *(Prázdné)* | ***1** _ | _*_Ano: US002_*_ | Ne | US003 | 3 | Ne | _ *US002** | **1** |
| *(Prázdné)* | ***1** _ | _*_Ano: US002_*_ | Ne | US003 | 3 | Ne | _ *US002** | **1** |
| *(Prázdné)* | 1 | Ne | Ano: 2 | ***US003** _ | _*_3_*_ | Ne | _ *US003** | **3** |
| *(Prázdné)* | 1 | Ne | ***Ano: 2** _ | _*_US003_*_ | 3 | Ano | _ *US003** | **2** |

## <a name="additional-resources"></a>Další prostředky

- [Nákupní smlouvy](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

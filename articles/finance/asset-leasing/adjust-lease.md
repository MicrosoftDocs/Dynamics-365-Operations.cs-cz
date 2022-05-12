---
title: Úprava leasingů
description: Toto téma vysvětluje, jak upravit leasing. Může být vyžadována úprava, pokud dojde ke změně podmínek leasingu, prodloužení leasingu nebo změně jiných okolností.
author: moaamer
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7d7151c28d124420638dc4e69a8ab5359ecf443c
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644548"
---
# <a name="adjust-leases"></a>Úprava leasingů

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak upravit leasing. Může být vyžadována úprava, pokud dojde ke změně podmínek leasingu, prodloužení leasingu nebo změně jiných okolností. Leasing majetku je v souladu s pokyny, které o změnách leasingu poskytuje téma Kodifikace účetních standardů 842 (ASC 842) a Mezinárodní standard finančního výkaznictví 16 (IFRS 16). ASC 842-20-15-1 definuje změnu leasingu jako jakoukoli změnu podmínek smlouvy, která způsobí změnu rozsahu nebo protiplnění leasingu. Odstavec 39 IFRS 16 stanovuje, že nájemce musí přehodnotit leasingový závazek tak, aby odpovídal změnám leasingových splátek.

U organizací, které dodržují standardy ASC 842 nebo IFRS 16, je leasing přeceňován tak, aby odpovídal drážel změnám současné hodnoty budoucích minimálních leasingových plateb (PVFMLP). Pokud se PVFMLP zvýší, bude vytvořená položka deníku debetem pro účet používaného majetku (ROU) a kreditem pro účet leasingového závazku vzhledem k rozdílu mezi novým PVFMLP a předchozím PVFMLP. Pokud PVFMLP poklesne, položka deníku bude debetem pro účet leasingového závazku a kreditem pro účet používaného majetku vzhledem k danému rozdílu.

Pokud úprava sníží používaný majetek na hodnotu menší 0 (nula), zbytek bude připsán k zisku na účet pro zaúčtování změny leasingu, který je uveden na stránce **Účty pro zaúčtování leasingu**. Systém účtuje tyto transakce a další položky úprav, jako jsou změny klasifikace, počáteční přímé náklady, pobídky k uzavření leasingové smlouvy, zálohy a náklady na demontáž, které vyplývají ze změn leasingu.

Konkrétní pokyny týkající se transakcí úpravy leasingu vám doporučujeme přečíst v IFRS 16 a ASC 842.

## <a name="lease-adjustment-wizard"></a>Průvodce úpravami leasingu

Pomocí následujících kroků upravíte leasing. Upravená data aktualizují plány leasingu poté, co provedete zaúčtování z průvodce **Úprava leasingu**. Svou práci můžete uložit a průvodce kdykoli zavřít a poté se vrátit zpět a pokračovat v práci.

Chcete-li otevřít průvodce **Úprava leasingu** ze shrnutí leasingu, postupujte podle těchto kroků.

1. Přejděte na **Leasing majetku \> Leasingy \> Shrnutí leasingu**. 
2. Vyberte leasing, který chcete upravit, a poté vyberte **Průvodce nastavením**.
3. Postupujte podle pokynů průvodce a zadejte požadované změny.

Chcete-li otevřít průvodce **Úprava leasingu** ze stránky **Úpravy leasingu**, u úpravy, která již probíhá, postupujte podle těchto kroků.

1.  Přejděte na **Leasing \> Leasingy \> Úpravy leasingu**.
2.  Vyberte leasing, který má stav úpravy **Probíhá** a potom vyberte **Průvodce nastavením**.
3.  Do polí **Datum zahájení úpravy** a **Datum zaúčtování** zadejte příslušná data.
4.  Zvolte **Další**.

    Leasing je nyní přidán na stránku **Úpravy leasingu**, kde můžete zadat nové informace.

    Po úpravě leasingu se na něj vztahují pole s ohledem na právo na užívání. Pokud se změněným leasingem nejsou spojeny žádné počáteční přímé náklady, pobídky k uzavření leasingové smlouvy, platby předem nebo náklady na demontáž, nechte příslušná pole prázdná. Původní částky se na aktualizovaný leasing nevztahují. 

    Pronajímatel například poskytuje pobídku 1000 USD za souhlas s prodloužením leasingu. V tomto případě, když upravíte leasing, aby se účtoval pro rozšíření, zadáte **1000** v poli **Pobídky k uzavření leasingové smlouvy na základě úpravy**.

    Řádky platebního plánu nyní zobrazují všechny platby z měsíce a pozdějších měsíců v poli **Datum zahájení úpravy**. Protože jsou úpravy prospektivní, řádky časového plánu plateb nelze spustit před zahájením úprav. Chcete-li zobrazit řádky časového plánu plateb před datem zahájení úpravy, přejděte na stránku **Historie verzí leasingu**.

8.  Zvolte **Další**.

    Na následující stránce jsou uvedeny klíčové informace o očekávané úpravě leasingu, například účetní hodnoty závazku z leasingu před úpravou a nový očekávaný závazek z leasingu po úpravě. Stránka také zobrazuje náhled položky deníku pro očekávanou úpravu leasingu.

9.  Možností **Odeslat do pracovního postupu** odešlete úpravu leasing do systému pracovního postupu, pokud je pracovní postup úpravy leasingu aktivní a úprava ještě nebyla schválena. Další informace o tom, jak používat pracovní postup úpravy leasingu, najdete v části [Použití pracovních postupů úpravy leasingu](use-create-lease-wrkflw.md).

    > [!NOTE]
    > V tomto okamžiku systém přepočítá proměnné úprav, aby ověřil, že proti leasingu nebyly zaúčtovány žádné transakce od doby, kdy byl poprvé vypočítán přehled úprav a položka deníku úprav. Pokud se některé hodnoty změní, aktualizuje se mřížka přehledu úprav a před opětovným odesláním úprav leasingu do systému pracovního postupu můžete tyto informace zkontrolovat.

10. Pokud pracovní postup není aktivní nebo pokud byla úprava leasingu schválena, vyberte **Dokončit**, aby se zpracovaly změny a zaúčtoval záznam deníku úprav.

    > [!NOTE] 
    > V tomto okamžiku systém přepočítá proměnné úprav, aby ověřil, že proti leasingu nebyly zaúčtovány žádné transakce od doby, kdy byl poprvé vypočítán přehled úprav a položka deníku úprav. Pokud se některé hodnoty změní, aktualizuje se mřížka přehledu úprav a před výběrem možnosti **Dokončit** můžete změny zkontrolovat. Pokud je pracovní postup aktivní a úprava leasingu byla schválena, jakékoli změny v přehledu úprav způsobí, že stav schválení bude nastaven zpět na **Neodesláno**. V takovém případě byste měli znovu odeslat úpravu leasing do systému pracovního postupu.

    Na stránce **Úpravy leasingu** je nyní stav úpravy nastaven na **Dokončeno**.

    Na stránce **Úpravy leasingu** stále můžete zobrazit pevné záložky **Přehled úprav** a **Náhled záznamu úpravy**. Podrobnosti o leasingu a datum jsou uvedeny v historii verzí daného pronájmu.

    Nová verze leasingu a nová sada plánů jsou nyní vytvořeny pomocí upravených informací. 

13. Chcete-li zobrazit nové plány, přejděte na leasing a poté vyberte **Knihy**.
14. Chcete-li zobrazit nově vygenerovaný plán plateb, vyberte **Platební plán**.
15. Chcete-li zobrazit nový plán amortizace leasingového závazku, který je generován z nových informací, zavřete stránku **Platební kalendář** a otevřete stránku **Plán amortizace závazku**.
16. Chcete-li zobrazit nově vygenerovaný plán odpisů aktiv, otevřete stránku **Plán odpisu majetku** ze stránky **Podrobnosti o knize**.
17. Chcete-li zobrazit položku deníku úpravy, vyberte **Deníky \> Deník leasingu majetku**.

## <a name="cancel-a-lease-adjustment"></a>Zrušení úpravy leasingu

Chcete-li odstranit probíhající úpravu leasingu, postupujte takto.

1.  Přejděte na **Leasing \> Leasingy \> Úpravy leasingu**.
2.  Vyberte probíhající úpravu leasingu, kterou chcete zrušit.
3.  Vyberte **Zrušit úpravu**. 
4.  Vyberte **OK**.

    > [!NOTE] 
    > Pokud vyberete **Zrušit** v průvodci **Úprava leasingu**, vrátíte zpět poslední změnu, kterou jste v průvodci provedli, ale neodstraníte probíhající úpravu.

## <a name="use-the-lease-adjustment-workflow"></a>Použití pracovního postupu úpravy leasingu

Tato část vysvětluje, jak používat pracovní postup úpravy leasingu. Pracovní postup úpravy leasingu vám pomůže spravovat úpravy leasingu konzistentním způsobem tím, že poskytne sadu kroků schválení a přiřadí je konkrétním uživatelům, kteří schválí úpravu leasingu dříve, než se stane konečnou. Po schválení úpravy leasingu v pracovním postupu můžete použít průvodce **Úprava leasingu** k provedení úpravy nájmu.

1.  Chcete-li odeslat úpravu leasingu ke schválení, přejděte na **Leasing \> Leasingy \> Úpravy leasingu**.
2.  Vyberte ID leasingu úpravy leasingu a poté vyberte **Průvodce nastavením**.
3.  Na poslední stránce průvodce vyberte **Odeslat ke schválení**.
4.  Zadejte komentář k úpravě a poté vyberte **OK**.

    Stav pracovního postupu se změní na **Čeká na schválení** a všechna pole v průvodci jsou uzamčena pro úpravy.

5.  Chcete-li úpravu leasingu schválit, přejděte na **Leasing \> Leasingy \> Úpravy leasingu**.
6.  Vyberte ID leasingu úpravy leasingu a zkontrolujte pevné záložky **Přehled úprav** a **Náhled záznamu úpravy**.
7.  Vyberte **Pracovní postup \> Schváleno**.

    Na stránce **Úpravy leasingu** je nyní stav pracovního postupu nastaven na **Schváleno**. V tomto okamžiku je úprava leasingu připravena k zaúčtování prostřednictvím položky deníku úprav.

8.  Chcete-li pokračovat ve zpracování úpravy leasingu a zaúčtování položky úpravy, přejděte na **Leasing \> Leasingy \> Úpravy leasingu**.
9.  Vyberte ID leasingu úpravy leasingu a poté vyberte **Průvodce nastavením**.
10. Vyberte **Další**, dokud se nedostanete na poslední stránku průvodce, a poté vyberte **Dokončit**.

Systém přepočítá účetní hodnoty leasingu, aby zajistil, že schválené proměnné úpravy jsou aktuální. Pokud dojde ke změnám, stav schválení se nastaví zpět na **Koncept** a musíte znovu odeslat úpravu leasingu do systému pracovního postupu.

## <a name="view-lease-versions"></a>Zobrazení verzí leasingu

Pokud byl leasing upraven, můžete zobrazit jeho různé verze. Můžete si také prohlédnout historické plány a podrobnosti o minulém leasingu.

1. Na stránce **Shrnutí leasingu** vyberte leasing a poté v podokně akcí vyberte **Historie verzí leasingu**.

    Pokud byl vybraný leasing upraven, stránka **Historie verzí leasingu** zobrazí jeho různé verze. Původní leasing je označen popiskem **1** a následující verze mají vzestupné číselné pořadí.

    U vybrané verze leasingu si můžete prohlédnout řádky finanční dimenze, podrobností smlouvy, umístění a platebního kalendáře.

2. Chcete-li zobrazit historické plány, otevřete upravený leasingu ze stránky **Souhrn leasingu**, vyberte požadovanou knihu a poté v podokně akcí vyberte **Historie verzí knihy**.
3. Na stránce **Verze knihy** vyberte verzi a plán, které chcete zobrazit.

## <a name="adjust-a-lease-book"></a>Úprava leasingové knihy

Chcete-li upravit pouze leasingovou knihu, postupujte následovně.

1. Přejděte na **Leasing majetku** \> **Leasingy** \> **Shrnutí leasingu**.
2. Vyberte a otevřete leasing.
3. Na stránce **Podrobnosti o leasingu** vyberte **Knihy**.
4. V podokně Akce na kartě **Podrobnosti o knize** ve skupině **Správa** vyberte **Upravit knihu**. 
5. Odeberte řádky platebního kalendáře.
6. V poli **Datum změny leasingu** zadejte datum změny. Poté zvažte odstranění všech dalších aspektů aktiv/pasiv (počáteční přímé náklady, pobídka k uzavření leasingové smlouvy, leasingové zálohy, náklady na demontáž a záruka zůstatkové hodnoty), pokud nějaké existují. 
7. Chcete-li předejít nepřesným výpočtům při úpravě leasingu, přidejte nové řádky plánu plateb pro nová data plateb, která odpovídají datu úpravy. 

> [!NOTE] 
> Při úpravě leasingu doporučujeme použít průvodce **Úprava leasingu**. Průvodce snižuje počet ručních kroků, poskytuje náhled zůstatků po úpravě a umožňuje změnit částky před zaúčtováním.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

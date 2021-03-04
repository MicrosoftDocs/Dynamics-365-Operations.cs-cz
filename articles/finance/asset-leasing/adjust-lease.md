---
title: Úprava leasingů
description: Toto téma vysvětluje, jak upravit leasing. Může být vyžadována úprava, pokud dojde ke změně podmínek leasingu, prodloužení leasingu nebo změně jiných okolností.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441369"
---
# <a name="adjust-leases"></a>Úprava leasingů

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak upravit leasing. Může být vyžadována úprava, pokud dojde ke změně podmínek leasingu, prodloužení leasingu nebo změně jiných okolností. Leasing majetku je v souladu s pokyny, které o změnách leasingu poskytuje téma Kodifikace účetních standardů 842 (ASC 842) a Mezinárodní standard finančního výkaznictví 16 (IFRS 16). ASC 842-20-15-1 definuje změnu leasingu jako jakoukoli změnu podmínek smlouvy, která způsobí změnu rozsahu nebo protiplnění leasingu. Odstavec 39 IFRS 16 stanovuje, že nájemce musí přehodnotit leasingový závazek tak, aby odpovídal změnám leasingových splátek.

U organizací, které dodržují standardy ASC 842 nebo IFRS 16, je leasing přeceňován tak, aby odpovídal drážel změnám současné hodnoty budoucích minimálních leasingových plateb (PVFMLP). Pokud se PVFMLP zvýší, bude vytvořená položka deníku debetem pro používaný majetek (ROU) a kreditem pro leasingový závazek vzhledem k rozdílu mezi novým PVFMLP a předchozím PVFMLP. Pokud PVFMLP poklesne, položka deníku bude debetem pro leasingový závazek a kreditem pro používaný majetek vzhledem k danému rozdílu.

Pokud úprava sníží používaný majetek na hodnotu menší 0 (nula), zbytek bude připsán k zisku na účet pro zaúčtování změny leasingu, který je uveden na stránce **Účty pro zaúčtování leasingu**. Systém účtuje tyto transakce a další položky úprav, jako jsou změny klasifikace, počáteční přímé náklady, pobídky k uzavření leasingové smlouvy, zálohy a náklady na demontáž, které vyplývají ze změn leasingu.

Konkrétní pokyny týkající se transakcí úpravy leasingu vám doporučujeme přečíst v IFRS 16 a ASC 842.

Chcete-li upravit leasing, postupujte následovně. Změněná data aktualizují plány leasingu, jakmile je spuštěn proces plánu vytvoření.

1. Přejděte na **Leasing majetku \> Leasingy \> Shrnutí leasingu**.
2. Na stránce **Shrnutí leasingu** vyberte leasing, který chcete upravit, a poté vyberte **Upravit leasing**.
3. Na stránce **Úprava leasingu** zadejte nové informace o upraveném leasingu.

    Všimněte si, že stránka **Úprava leasingu** se podobá stránce **Přidání leasingu**. Kromě toho, stejně jako datum zahájení, které zadáte při přidání leasingu, určuje zahájení leasingu, pole **Datum změny** na stránce **Úprava leasingu** určuje zahájení změněného leasingu. Toto datum nesmí být po počátečním datu v řádcích platebního kalendáře.

    > [!NOTE]
    > Pole **Protihodnota používaného majetku** se vztahují na úpravu nájmu. Pokud se změněným leasingem nejsou spojeny žádné počáteční přímé náklady, pobídky k uzavření leasingové smlouvy, platby předem nebo náklady na demontáž, měli byste tato pole nechat prázdná. Původní částky se na aktualizovaný leasing nevztahují. Veškeré dodatečné náklady, které vzniknou při změně leasingu, by měly být uvedeny na stránce **Úprava leasingu**.
    > 
    > Pronajímatel například poskytuje pobídku 1000 USD za souhlas s prodloužením leasingu. V tomto případě, když upravíte leasing, aby se účtoval pro rozšíření, zadáte **1000** v poli **Pobídky k uzavření leasingové smlouvy**. Pokud s úpravou leasingu nejsou spojeny žádné pobídky, měli byste vymazat hodnotu, kterou jste dříve zadali do tohoto pole. Stejná logika platí pro další protihodnoty používaného majetku.

    Řádky platebního kalendáře upraveného leasingu by měly být vytvořeny přeběžně. Řádky platebního kalendáře, které jsou vytvořeny předběžně, nemohou být zahájeny, než se projeví úpravy leasingu.

    Následující kroky jsou téměř identické s kroky pro počáteční uznání leasingu.

4. Vyberte **Vytvořit plány** pro vygenerování upraveného platebního kalendáře. Zobrazí se zpráva s oznámením, že byl vytvořen platební kalendář pro leasing.

    > [!IMPORTANT]
    > Než vyberete **Vytvořit plány**, ujistěte se, že řádky data změny a platebního kalendáře jsou přesné. Také se ujistěte, že všechny počáteční přímé náklady, pobídky k uzavření leasingové smlouvy, zálohy nebo náklady na demontáž odpovídají pouze těm nákladům, které vzniknou z úpravy.

5. Chcete-li zobrazit nově vytvořený platební kalendář, vyberte **Knihy** a otevřete stránku **Platební kalendář**.
6. Na stránce **Platební kalendář** můžete upravit upravené částky plateb, než potvrdíte platební kalendář. Pro potvrzení kalendáře vyberte **Potvrdit kalendář**.

    Po potvrzení platebního kalendáře se vytvoří nové odpisy majetku a nové plány leasingových závazků.

7. Chcete-li zobrazit nový plán amortizace leasingového závazku, který je generován z nových vstupů, zavřete stránku **Platební kalendář** a otevřete stránku **Plán amortizace závazku**.
8. Chcete-li zobrazit nově vygenerovaný plán odpisů aktiv, otevřete stránku **Plán odpisu majetku** ze stránky **Podrobnosti o knize**.
9. Chcete-li vygenerovat položku deníku úpravy, vyberte **Funkce \> Úprava leasingu**. Zobrazí se zpráva, že byla vytvořena položka deníku úpravy. 
10. Chcete-li zobrazit položku deníku, vyberte **Deníky \> Deník leasingu majetku**.
11. Chcete-li zaúčtovat položku deníku, vyberte řádek a poté vyberte **Zaúčtovat**.

## <a name="view-lease-versions"></a>Zobrazení verzí leasingu

Pokud byl leasing upraven, můžete zobrazit jeho různé verze. Můžete si také prohlédnout historické plány a podrobnosti o minulém leasingu.

1. Na stránce **Shrnutí leasingu** vyberte leasing a poté v podokně akcí vyberte **Historie verzí leasingu**.

    Pokud byl vybraný leasing upraven, stránka **Historie verzí leasingu** zobrazí jeho různé verze. Původní leasing je označen popiskem **1** a následující verze mají vzestupné číselné pořadí.

    U vybrané verze leasingu si můžete prohlédnout řádky finanční dimenze, podrobností smlouvy, umístění a platebního kalendáře.

2. Chcete-li zobrazit historické plány, otevřete upravený leasingu ze stránky **Souhrn leasingu**, vyberte požadovanou knihu a poté v podokně akcí vyberte **Historie verzí knihy**.
3. Na stránce **Verze knihy** vyberte požadovanou verzi a požadovaný plán, které chcete zobrazit.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
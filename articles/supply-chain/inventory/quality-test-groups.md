---
title: Testovací skupiny pro řízení kvality
description: Tento článek popisuje, jak vytvořit testovací skupiny, aby bylo možné použít více testů s objednávkami kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7722bc92d8c2bf52d6a798a93f07af44037d4e0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857686"
---
# <a name="quality-management-test-groups"></a>Testovací skupiny pro řízení kvality

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak vytvořit testovací skupiny, aby bylo možné použít více testů s objednávkami kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.

Použijte stránku **Testovací skupiny** k nastavení, úpravě a zobrazení testovacích skupin a jednotlivých testů přiřazených testovacím skupinám. V horní části stránky jsou zobrazeny testovací skupiny a v dolní části jsou zobrazeny testy, které jsou přiřazené vybrané testovací skupině.

Každé testovací skupině můžete přiřadit několik zásad, jako je plán vzorkování, přijatelné úrovně kvality (AQL) a požadavky na destrukční testy. Poté při přiřazení jednotlivého testu do testovací skupiny definujete další informace, jako jsou například pořadí, dokumenty nebo data platnosti. Pro kvantitativní test definujete také informace o přijatelných hodnotách měření. Informace o testu kvality obsahují také testovací proměnné a výchozí výstup.

Skupina testů přiřazená objednávce kvality určuje výchozí sadu testů, které je nutné na určených položkách vykonat. Testy však můžete přidat, odstranit nebo změnit pro objednávku kvality. Výsledky testu jsou uvedeny pro všechny testy v objednávce kvality.

Když definujete testovací skupinu, můžete volitelně určit vzorkování položky. Vzorkování položek se používá k definování množství produktu, které musí být testováno. Další informace viz [Vzorkování položek řízení jakosti](quality-item-sampling.md). Můžete také určit, zda jsou testy v testovací skupině destruktivní. Při destruktivním testu je vzorkování položky zničeno a množství je odstraněno ze zásob na skladě.

## <a name="example-of-a-test-group"></a>Příklad testovací skupiny

Výrobní společnost má definované testovací skupiny pro každou variantu pokynů týkajících se kvality. Různé testovací skupiny odrážejí rozdíly v plánech vzorkování, v sadách testů, které je nutné provádět dohromady, v přijatelné úrovni kvality i v dalších činitelích. Pro kvantitativní testy existují také rozdíly v přijatelných hodnotách měření. K vynucení svých pokynů pro kvalitu společnost přiřadí ke každému pravidlu testovací skupinu, která se používá k automatickému generování objednávek kvality na stránce **Přidružení kvality**. Přiřadí také testovací skupinu k objednávkám kvality, které jsou vytvořeny ručně.

## <a name="create-a-test-group"></a>Vytvoření testovací skupiny

Pokud chcete vytvořit testovací skupinu, postupujte takto.

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Testovací skupiny**.
1. V podokně akcí vyberte možnost **Nový**, a přidejte tak řádek do mřížky v horní části stránky. Poté pro nový řádek nastavte následující pole:

    - **Testovací skupina** – zadejte jedinečné ID nebo název testovací skupiny.
    - **Popis** – zadejte podrobný popis testovací skupiny.
    - **Přijatelná úroveň kvality** – zadejte celkové procento výsledků testů, které musí vyhovět, aby mohla být skupina testů považována za splněnou.
    - **Vzorkování položek** – vyberte vzorkování položky. Další informace viz [Vzorkování položek řízení jakosti](quality-item-sampling.md).
    - **Destruktivní** – zaškrtnutím tohoto políčka označíte, že testovací skupina zničí položky, které jsou testovány.

1. Zatímco je stále vybrán nový řádek, vyberte kartu **Obecné** v horní části stránky. Některá nastavení pro testovací skupinu, která je vybrána na kartě **Přehled**, se zde opakují. Kromě toho můžete pro skupinu nastavit následující pole:

    - **Aktualizovat atribut skladové dávky** – když zde nastavíte tuto možnost na hodnotu *Ano*, automaticky se nastaví na *Ano* pro každý nový test, který je přidán do testovací skupiny v dolní části stránky.
    - **Aktualizovat dispozici dávky** – když nastavíte tuto možnost na hodnotu *Ano*, pokud je položka, která je testována, dávkově řízena, bude dispozice dávky automaticky aktualizována o hodnotu, která je vybrána v poli **Dispozice dávky objednávky kvality se nezdařila** nebo **Dispozice dávky platné objednávky kvality**.
    - **Dispozice dávky objednávky kvality se nezdařila** – vyberte dispoziční kód dávky, který by měl být přiřazen, když selže objednávka kvality, která zahrnuje tuto testovací skupinu, protože nesplňuje požadavky AQL.
    - **Dispozice dávky platné objednávky kvality** – vyberte dispoziční kód dávky, který by měl být přiřazen, když úspěšně projde objednávka kvality, která zahrnuje tuto testovací skupinu, protože splňuje požadavky AQL.
    - **Aktualizovat stav zásob** – když nastavíte tuto možnost na hodnotu *Ano*, pokud je povolena možnost **Stav zásob** ve skupině dimenze úložiště pro položku, která je testována, bude stav automaticky aktualizován o stav vybraný v poli **Stav objednávky kvality Neúspěch** nebo **Stav objednávky kvality Úspěch**.
    - **Stav objednávky kvality Neúspěch** – vyberte stav zásob, který by měl být přiřazen položce, když selže objednávka kvality, která zahrnuje tuto testovací skupinu, protože nesplňuje požadavky AQL.
    - **Stav objednávky kvality Úspěch** – vyberte stav zásob, který by měl být přiřazen položce, když úspěšně projde objednávka kvality, která zahrnuje tuto testovací skupinu, protože splňuje požadavky AQL.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Přidání testu kvality do testovací skupiny

Chcete-li do testovací skupiny přidat test kvality, postupujte takto.

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Testovací skupiny**.
1. Na kartě **Přehled** vyberte v horní části stránky testovací skupinu, do které chcete přidat test.
1. Ve spodní části stránky vyberte na kartě **Přehled** na panelu nástrojů možnost **Přidat**, a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Pořadové číslo** – zadejte celé číslo a určete pořadí, ve kterém by se testy měly provádět. Testy, které mají menší pořadová čísla, budou spuštěny před testy, které mají větší pořadová čísla.

        > [!NOTE]
        > Doporučujeme ponechat mezeru mezi pořadovými čísly. Například nastavte pole **Pořadové číslo** na hodnotu *10* pro svůj první test a poté zvyšte hodnotu o 10 pro každý další test. Tímto způsobem můžete přidat později nové testy, aniž byste museli mazat a znovu vytvářet řádky, aby byly v požadovaném pořadí.

    - **Test** – vyberte testy, které chcete provést. Pro test kvality vyberte test, kde je pole **Typ** nastaveno na hodnotu *Možnost*.
    - **Účinné** – vyberte první datum, kdy je test platný. Pokud ponecháte toto pole prázdné, nebude žádné omezení.
    - **Vypršení platnosti** – vyberte poslední datum, kdy je test platný. Necháte-li toto pole prázdné nebo nastavíte na hodnotu *Nikdy*, nebude žádné omezení.
    - **Určení testovací hodnoty** – vyberte, jak má být určeno AQL, když je pro stejný test zaznamenáno více výsledků. Pro test kvality lze vybrat pouze možnost *Ruční*. Pokud vyberete jednu z dalších hodnot (*Průměrný*, *Minimum* nebo *Maximum*), při uložení testovací skupiny se zobrazí chybová zpráva.
    - **Atribut** – chcete-li zaznamenat výsledky testu na atribut dávky, vyberte zde atribut a vyberte zaškrtávací políčko **Aktualizovat atribut skladové dávky**.
    - **Aktualizovat atribut skladové dávky** – výběrem tohoto zaškrtávacího políčka zaznamenáte výsledky testu pro atribut dávky, který je vybrán v poli **Atribut**.

1. Ve spodní části stránky vyberte kartu **Obecné**. Některá nastavení pro test, který je vybrán na kartě **Přehled**, se zde opakují. Kromě toho můžete pro test nastavit následující pole:

    - **Certifikát pro sestavu analýzy** – nastavte tuto možnost na hodnotu *Ano* označující, že výsledky testu by měly být vytištěny na certifikátu analýzy (CoA). Tuto sestavu lze vygenerovat z objednávky kvality.
    - **Akce při selhání** – vyberte buď hodnotu *Přijmout*, nebo *Neúspěch* k označení, zda by měl test vyhovět nebo neuspět, pokud není splněna AQL.
    - **Přijatelná úroveň kvality** – zadejte celkové procento výsledků testů, které musí vyhovět, aby mohl být test považován za splněný.

1. Ve spodní části stránky na kartě **Test** nastavte následující pole:

    - **Proměnná** – vyberte proměnnou testu určenou pro zaznamenání výsledků testu kvality.
    - **Výchozí výsledek** – vyberte výchozí výsledek, který by měl být zaznamenán pro výsledky testu.
    - **Testovací přístroj** – vyberte zařízení, které má být použito pro test. Pokud je definován testovací přístroj, je automaticky zadán pro test v testovací skupině.

1. Zavřete stránku.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Přidání testu množství do testovací skupiny

Chcete-li do testovací skupiny přidat test množství, postupujte takto.

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Testovací skupiny**.
1. Na kartě **Přehled** vyberte v horní části stránky testovací skupinu, do které chcete přidat test.
1. Ve spodní části stránky vyberte na kartě **Přehled** na panelu nástrojů možnost **Přidat**, a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Pořadové číslo** – zadejte celé číslo a určete pořadí, ve kterém by se testy měly provádět. Testy, které mají menší pořadová čísla, budou spuštěny před testy, které mají větší pořadová čísla.

        > [!NOTE]
        > Doporučujeme ponechat mezeru mezi pořadovými čísly. Například nastavte pole **Pořadové číslo** na hodnotu *10* pro svůj první test a poté zvyšte hodnotu o 10 pro každý další test. Tímto způsobem můžete přidat později nové testy, aniž byste museli mazat a znovu vytvářet řádky, aby byly v požadovaném pořadí.

    - **Test** – vyberte testy, které chcete provést. Pro test množství vyberte test, kde je pole **Typ** nastaveno na hodnotu *Zlomek* nebo *Celé číslo*.
    - **Účinné** – vyberte první datum, kdy je test platný. Pokud ponecháte toto pole prázdné, nebude žádné omezení.
    - **Vypršení platnosti** – vyberte poslední datum, kdy je test platný. Necháte-li toto pole prázdné nebo nastavíte na hodnotu *Nikdy*, nebude žádné omezení.
    - **Určení testovací hodnoty** – vyberte, jak má být určeno AQL, když je pro stejný test zaznamenáno více výsledků. Dostupné možnosti jsou *Průměrný*, *Minimum*, *Maximum* a *Ruční*.
    - **Atribut** – chcete-li zaznamenat výsledky testu na atribut dávky, vyberte zde atribut a vyberte zaškrtávací políčko **Aktualizovat atribut skladové dávky**.
    - **Aktualizovat atribut skladové dávky** – výběrem tohoto zaškrtávacího políčka zaznamenáte výsledky testu pro atribut dávky, který je vybrán v poli **Atribut**.

1. Ve spodní části stránky vyberte kartu **Obecné**. Některá nastavení pro test, který je vybrán na kartě **Přehled**, se zde opakují. Kromě toho můžete pro test nastavit následující pole:

    - **Certifikát pro sestavu analýzy** – nastavte tuto možnost na hodnotu *Ano* označující, že výsledky testu by měly být vytištěny na certifikátu analýzy. Tuto sestavu lze vygenerovat z objednávky kvality.
    - **Akce při selhání** – vyberte buď hodnotu *Přijmout*, nebo *Neúspěch* k označení, zda by měl test vyhovět nebo neuspět, pokud není splněna AQL.
    - **Přijatelná úroveň kvality** – zadejte celkové procento výsledků testů, které musí vyhovět, aby mohl být test považován za splněný.

1. Ve spodní části stránky na kartě **Test** nastavte následující pole:

    - **Standardní** – zadejte množství (celé číslo nebo zlomek), která se očekává pro výsledky testu. Hodnota, kterou zadáte, bude ve výchozím nastavení zadána do výsledků testu. Navíc bude automaticky zadána jako výchozí hodnota do polí **Minimum** a **Maximum**.
    - **Minimum** – zadejte minimální povolenou hodnotu pro výsledky testu. Hodnota, kterou zadáte, musí být menší než množství nastavené v poli **Standardní**. Při aktualizaci pole **Minimum** se pole **Minimální tolerance (%)** automaticky aktualizuje. Podobným způsobem se při aktualizaci pole **Minimální tolerance (%)** automaticky aktualizuje pole **Minimum**.
    - **Maximum** – zadejte maximální povolenou hodnotu pro výsledky testu. Hodnota, kterou zadáte, musí být větší než množství nastavené v poli **Standardní**. Při aktualizaci pole **Maximum** se pole **Maximální tolerance (%)** automaticky aktualizuje. Podobným způsobem se při aktualizaci pole **Maximální tolerance (%)** automaticky aktualizuje pole **Maximum**.
    - **Testovací přístroj** – vyberte zařízení, které má být použito pro test. Pokud je definován testovací přístroj, je automaticky zadán pro test v testovací skupině.

1. Zavřete stránku.

## <a name="additional-resources"></a>Další prostředky

- [Testovací přístroje pro řízení kvality](quality-management-processes.md)
- [Testy správy kvality](quality-management-processes.md)
- [Testovací proměnné pro řízení kvality](quality-management-processes.md)
- [Přiřazení kvality](quality-management-processes.md)
- [Atributy dávky](../production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

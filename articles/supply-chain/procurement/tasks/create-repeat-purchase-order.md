---
title: Vytvoření opakované nákupní objednávky
description: Tento článek popisuje, jak vytvořit opakující se nákupní objednávky zkopírováním řádků z předchozího dokumentu nákupní objednávky do nové či stávající nákupní objednávky.
author: GalynaFedorova
ms.date: 09/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335461d60fa0bc92e9711806c6e42643a3f75d02
ms.sourcegitcommit: 073604c07116e0a87f78ab2c76cb89ae83ebba3c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608099"
---
# <a name="create-a-repeat-purchase-order"></a>Vytvoření opakované nákupní objednávky

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak vytvořit opakující se nákupní objednávky zkopírováním řádků z předchozího dokumentu nákupní objednávky do nové či stávající nákupní objednávky. Existují dva způsoby vytvoření opakovaných objednávek. Můžete použít akce dostupné na úrovni dokumentů v podokně akcí, nebo můžete použít akce z podrobností o řádku. Akce na úrovni dokumentu jsou určeny k vytvoření nové nákupní objednávky přidáním řádků a informací ze záhlaví z jiné objednávky, zatímco akce z podrobností řádku se používá zejména pro přidávání řádků do existující objednávky. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Tento úkol obvykle provádí nákupčí.

## <a name="create-a-new-repeat-purchase-order"></a>Vytvoření nové opakující se nákupní objednávky

1. V navigačním podokně přejděte na **Moduly \> Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**. Nejprve vyzkoušíme možnost zkopírovat informace do nové objednávky.  
1. Zvolte **Nové**.
1. Do pole **Účet dodavatele** zadejte `US-101`.
1. Vyberte **OK**.
1. V podokně akcí otevřete kartu **Nákupní objednávka** a ve skupině **Kopírovat** vyberte **Ze všech**. Otevře se dialogové okno **Kopírovat z jiných dokumentů**. Odsud můžete kopírovat údaje z existující objednávky do své objednávky. Existují různé možnosti, jak lze řádky kopírovat, a různé typy dokumentů, ze kterých lze kopírovat. Podíváme se nejprve na možnosti, jak kopírovat řádky.
1. Rozbalte pevnou záložku **Parametry**.

    - Pole **Koeficient množství** je užitečné, když je nutné použít množství, které se liší od množství v objednávce, ze které kopírujete. Například pokud chcete objednat dvakrát takové množství, než které je v řádcích, ze kterých kopírujete, zadejte do tohoto pole "2" a systém přidá řádky, kde je dvojnásobné původní množství.  
    - Pole **Opačné znaménko** podporuje také změnu objednaného množství změnou znaménka u množství na přidaných řádcích v objednávce. To může být užitečné v případě, že je nutné stornovat transakci vytvořením řádků objednávky, které negují transakci. Tato možnost je vybrána automaticky při otevření stránky akcí **Vytvoření dobropisu**.  
    - Možnost **Kopírovat náklady** umožňuje kopírovat náklady do nové objednávky z dokumentu, ze kterého kopírujete řádky objednávky.  
    - Možnost **Přepočítat ceny** používá aktuální ceny a slevy namísto jejich kopírování z dokumentu, ze kterého kopírujete ostatní informace.  
    - Možnost **Přesná kopie** zkopíruje hodnoty několika polí v záhlaví a řádcích objednávky. Pokud tuto možnost nevyberete, výchozí hodnoty budou použity pro mnoho polí týkajících se dodavatele a produktů, stejně jako byste vytvářeli novou objednávku ručně. Například pokud nastavíte možnost **Přesná kopie** na *Ano* a zkopírujete objednávku, která přepíše výchozí účet faktury pro dodavatele, poté bude do nové objednávky zkopírován stejný účet faktury. Pokud nastavíte možnost **Přesná kopie** na *Ne*, ve vaší nové objednávce se namísto toho použije výchozí účet faktury pro dodavatele. Když je možnost **Přesná kopie** nastavena na *Ano*, zkopírují se hodnoty pro následující pole:
        - Jazyk
        - Platební podmínky
        - Metoda platby
        - Určení platby
        - Skupina číselné řady
        - Platební sleva
        - Procento slevy
        - Měna
        - Dodací podmínky
        - Způsob dodání
        - Dimenze
        - Skupina DPH
        - Přepsat DPH
        - Ceny zahrnují DPH.
        - Přeprava
        - Přístav
        - Statistická procedura
        - ID šablony
        - Název dodávky
        - Poštovní adresa
        - Reference
        - ID referenční tabulky
    - Možnost **Odstranit řádky nákupu** odstraní všechny řádky nákupní objednávky, které již existují v nákupní objednávce, do které kopírujete, a to před použitím nových řádků. Tuto možnost použijte opatrně, protože odstraní všechny stávající řádky bez dalšího upozornění.  
    - Pokud použijete možnost **Kopírovat záhlaví objednávky**, nemusíte ručně vytvářet informace o záhlaví v nové objednávce. Tato možnost bude mít za následek použití výchozích hodnot pro pole související s dodavatelem. Pokud dokument, ze kterého kopírujete, má jiné než výchozí hodnoty, které chcete zkopírovat, použijte také možnost **Přesná kopie**.
    - Existují různé zdroje dokumentů, ze kterých lze kopírovat, a každý má určenou samostatnou část na této stránce. Například část **Nákupní objednávky** umožňují kopírovat z existujících nákupních objednávek.  

1. V části **Nákupní objednávky** vyberte řádky, které chcete zkopírovat do schránky. Je možné vybrat další řádky nákupní objednávky z jiných nákupních objednávek a zkopírovat je také do objednávky. Také je možné přidat řádky z jiných typů dokumentů pro nákup. Dalších několik kroků umožňuje prohlédnout různé možnosti.  
1. Rozbalte sekci **Potvrzení**. Zde můžete vybrat potvrzení nákupních objednávek, ze kterých chcete kopírovat. Potvrzení nákupních objednávek jsou označena pomocí ID přidruženého deníku nákupu nebo ID nákupní objednávky.  
1. Rozbalte část **Příjemky produktu**. Zde můžete vybrat deníky příjemek produktu, ze kterých chcete kopírovat. Deníky příjemek produktu jsou označeny dokladem produktu dodávky nebo ID nákupní objednávky.
1. Rozbalte sekci **Faktury**. Zde můžete vybrat faktury dodavatele, ze kterých chcete kopírovat. Faktury jsou označeny dokladem faktury nebo ID nákupní objednávky.
1. Rozbalte sekci **Vybrané řádky nebo záhlaví ke zkopírování**. Toto zobrazení obsahuje přehled všech dokladů a řádků, které byly vybrány, a ze kterých budete kopírovat do své objednávky.
1. Vyberte **OK**. Vybrané řádky byly zkopírovány do nové nákupní objednávky.

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopírování řádků do existující nákupní objednávky  

Místo kopírování celé objednávky je běžnější vytvořit novou nákupní objednávku a vyplnit informace v záhlaví nákupní objednávky, a pak jednotlivé řádky kopírovat z existujících objednávek.  

1. Vyberte **Řádek nákupní objednávky**.
1. Vyberte **Ze všeho**. Nově otevřená stránka je stejná jako stránka otevřená dříve, ale při otevření ze zobrazení řádků objednávky jsou vybrány jiné možnosti. Zkontrolujme si parametry.
1. Rozbalte sekci **Parametry**.

    - Možnost **Odstranit řádky nákupu** není vybrána. To znamená, že můžete kopírovat nové řádky do objednávky bez odstranění existujících řádků.
    - Možnost **Kopírovat záhlaví objednávky** také není vybrána, protože pouze přidáváme další řádky do objednávky.
    - V tomto příkladu si zkopírujeme řádky z existující nákupní objednávky.

1. Zvolte řádek pro požadovanou nákupní objednávku. Všimněte si, že byl vybrán také jeden řádek objednávky v této nákupní objednávce.  
1. Vyberte **OK**. Další řádek objednávky byl přidán do nákupní objednávky.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
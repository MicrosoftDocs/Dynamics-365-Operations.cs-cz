---
title: Nastavení směrnice skladového místa pro vyskladnění v rámci nákupní objednávky
description: Tento článek vysvětluje, jak nastavit jednoduchou směrnici umístění.
author: Weijiesa
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25484efd7be026bfc3a209fb52822b87d6b76cc2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065487"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Nastavení směrnice skladového místa pro vyskladnění v rámci nákupní objednávky

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak nastavit jednoduchou směrnici umístění. Uvedený příklad vytvoří směrnici skladového místa, který má být použita k určení umístění položek, které byly přijaty pro nákupní objednávku. Tohoto průvodce úkolem můžete použít s uvedenými daty za použití ukázkových dat společnosti USMF. Předpoklady: Je nutné vytvořit dispoziční kód. V tomto postupu používáme dispoziční kód Relabel. Pokud vytváříte směrnici skladového místa ve vlastních datech, je nutné nastavit pro sklad a položky procesy správy skladu (WMS). Tento postup je určen pro vedoucího skladu.

1. V navigačním podokně přejděte na **Moduly > Řízení skladu > Nastavení > Vlny > Směrnice umístění**.
2. V poli **Typ pořadí pracovních činností** vyberte možnost **Nákupní objednávky**.

## <a name="create-a-location-directive-header"></a>Vytvoření záhlaví směrnice skladového místa
1. Zvolte **Nové**.
2. V poli **Pořadové číslo** zadejte číslo. Toto je pořadí, ve kterém je zpracována směrnice skladového místa pro vybraný typ práce. Pořadí můžete v případě potřeby změnit.  
3. Zadejte hodnotu do pole **Název**. Toto je jedinečný identifikátor pro tuto směrnici.  
4. V poli **Typ práce** vyberte **Vložit**. Vybrat typ práce, která má být vykonávána. **Vložit** je jediná podporovaná hodnota pro směrnici s typem pořadí pracovních činností Nákupní objednávka.  
5. Zadejte hodnotu do pole **Pracoviště**.
6. Zadejte hodnotu do pole **Sklad**. Pole Kód předpisu nevyplňujte.  Kódy předpisů umožňují propojit řádek pořadí pracovních činností typu Vložit s konkrétním předpisem. Pro nákupní objednávky se umístění posledního řádku pořadí pracovních činností typu Vložit přeloží předtím, než je určena šablona práce. Proto není možné připojit poslední řádek šablony práce k určitému předpisu.   
7. Zadejte hodnotu do pole **Dispoziční kód**. Dispoziční kód omezuje použití směrnice skladového místa, aby se směrnice skladového místa používala, jen pokud pracovník skladu zadá tuto konkrétní hodnotu během registrace položky pomocí mobilního zařízení.  
8. Zvolte **Uložit**.

## <a name="edit-the-query-for-directive"></a>Úprava dotazu pro směrnici
1. Vyberte **Upravit dotaz**. Použití této směrnice již omezené pro položky, které jsou registrovány do skladu, který jste zadali, a s dispozičním kódem, který jste zadali. Pomocí dotazu můžete přidat další omezení.  
2. Vyberte **OK**.

## <a name="add-directive-lines"></a>Přidání řádků směrnice
1. Zvolte **Nové**. Toto je pořadí, ve kterém jsou zpracovány řádky předpisu skladového místa pro vybraný typ práce. Pořadí můžete v případě potřeby změnit.  
2. V poli **Od množství** zadejte číslo. Toto je minimální množství, pro které platí tento řádek směrnice.  
3. Zadejte číslo do pole **Do množství**.
4. Do pole **Jednotka** zadejte hodnotu. Jednotka hodnoty Od množství a Do množství. Pokud toto pole zůstane prázdné, bude použita skladová položka z této položky.  
5. Vyberte volbu v poli **Vyhledat množství**.
    - Žádné množství nebo množství registrační značky – množství: Množství registrované pro každou registrační značku.  
    - Sjednocené množství: Celé množství, které bylo registrováno.  
    - Zbývající množství: Množství, které má být teprve registrováno z řádku nákupní objednávky.  
    - Očekávané množství: Celkové množství zadané na řádku nákupní objednávky.  
6. Zaškrtněte nebo zrušte zaškrtnutí políčka **Omezit podle jednotky**. Pokud vyberete tuto možnost a určíte jednotku na stránce **Omezit podle jednotky**, do skladového místa lze umístit jen položky s touto jednotkou měření. Například pokud je měrná jednotka PL (palety), na určité skladové místo lze umístit jen položky na paletách.  
7. Zaškrtněte nebo zrušte zaškrtnutí políčka **Povolit rozdělení**. Umožňuje, aby směrnice rozdělila množství do více skladových míst.  
8. Zvolte **Uložit**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Omezení řádku směrnice na konkrétní jednotku
1. Vyberte **Omezit podle jednotky**. Toto tlačítko je k dispozici pouze v případě, že stisknete **Uložit** po zaškrtnutí políčka **Omezit podle jednotky**.  
2. Do pole **Jednotka** zadejte hodnotu.
3. Zavřete stránku.

## <a name="add-a-location-directive-action-line"></a>Přidání řádku akce směrnice pro skladová místa
1. Zvolte **Nové**. Toto je pořadí, ve kterém jsou zpracovány řádky akcí předpisu skladového místa pro vybraný typ práce. Pořadí můžete v případě potřeby změnit.  
2. Zadejte hodnotu do pole **Název**. Toto je jedinečný identifikátor pro tuto akci směrnice.  
3. Vyberte volbu v poli **Využití pevného skladového místa**.
    - Pevná a ostatní skladová místa: Všechna jiná než pevná skladová místa jsou platná stejně jako vlastní pevné skladové místo produktu v zadaném rozsahu v dotazu.  
    - Pouze pevná skladová místa pro produkt: Pevná skladová místa produktu jsou platná a všechny varianty produktu sdílejí stejnou skupinu pevných skladových míst.  
    - Pouze pevná skladová místa pro variantu produktu: Jsou platná pouze pevná skladová místa, která jsou zadaná pro každou variantu produktu.  
4. Vyberte volbu v poli **Strategie**. Pracovní příkazy typu nákupní objednávky podporují následující strategie: 
    - Žádné: položka bude umístěna v prvním nalezeném umístění.  
    - Konsolidovat: Položka je umístěna na skladové místo, kde jsou již k dispozici podobné položky.  
    - Prázdné umístění s žádnou příchozí prací: Položka je umístěna na první prázdné nalezené skladové místo. Skladové místo je považováno za prázdné, pokud nemá žádné fyzické zásoby a neočekává příchozí práci.  
5. Zvolte **Uložit**.

## <a name="edit-the-query-for-directive-action-line"></a>Úprava řádku akce dotazu pro směrnici
1. Vyberte **Upravit dotaz**.
2. Vyberte **přidat**.
3. Zadejte hodnotu `location profile ID` do pole **Pole**. V tomto příkladu omezíme možná skladová místa pomocí ID profilu skladového místa.  
4. Zadejte hodnotu do pole **Kritéria**.
5. Vyberte **OK**. Můžete pokračovat v přidávání řádků směrnice a akcí směrnice, dokud nebudete mít pokryty všechny možné scénáře skladu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
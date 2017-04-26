---
title: "Nastavení rozložení obrazovky pro POS"
description: "Toto téma obsahuje informace o rozložení obrazovky pro 365 Microsoft Dynamics pro operace - maloobchodní místa prodeje (POS) zkušenosti."
author: josaw1
manager: AnnBe
ms.date: 2016-06-09 20 - 55 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Nastavení rozložení obrazovky pro POS

Toto téma obsahuje informace o rozložení obrazovky pro 365 Microsoft Dynamics pro operace - maloobchodní místa prodeje (POS) zkušenosti.

365 Microsoft Dynamics pro operace - prodejní místa prodeje (POS) uživatelské rozhraní lze konfigurovat pomocí kombinace vizuální profily a rozložení obrazovky, přiřadit obchody, registry nebo uživatelům.

## <a name="visual-profile"></a>Vizuální profil
Vizuální profily jsou přiřazeny registry a slouží k určení vizuální prvky, které jsou specifické pro evidenci a sdílené mezi uživateli. Libovolný uživatel, který se přihlásí do rejstříku bude mít stejný motiv, barvy a obrázky. **Číslo profilu** -číslo profilu je jedinečný identifikátor pro vizuální profil. **Popis** -popis umožňuje zadat smysluplný název, který vám pomůže identifikovat správný profil pro danou situaci. **Motiv** -uživatelé mohou zvolit mezi motivy aplikace světlé nebo tmavé. Tato nastavení ovlivňují barvu písma a pozadí v rámci aplikace. **Barva zvýraznění** -barva zvýraznění v celém POS slouží k odlišení nebo zvýraznit některé vizuální prvky, jako jsou dlaždice, příkazová tlačítka nebo hypertextové odkazy. Tyto prvky jsou obvykle napadnutelné. **Barva záhlaví** -barva záhlaví umožňuje uživateli konfigurovat barvu záhlaví stránky pro vlastní potřeby prodejce. Tato funkce je pouze k dispozici v Dynamics 365 verzi operace 1611. **Přihlašovací pozadí** -uživatelé mohou zadat obrázek pozadí pro přihlašovací obrazovku. Velikost obrázků na pozadí je třeba uchovávat co nejmenší, jako je ukládání a načítání velkých souborů může mít vliv na chování aplikace a výkonu. **Pozadí aplikace** -The POS můžete také použít obrázek jako pozadí v aplikaci místo plné motivu barvu. Stejně jako u přihlašovací pozadí, by měl udržet co nejmenší velikost souboru.

## <a name="screen-layouts"></a>Rozložení obrazovky
Konfigurace rozložení obrazovky určuje akce, obsah a umístění ovládacích prvků uživatelského rozhraní v POS úvodní obrazovku a obrazovku transakce. ** Úvodní obrazovku **-ve většině případů je uvítací stránky, které uživatelé uvidí při prvním přihlášení do POS. Úvodní obrazovka může obsahovat obrázek značky a mřížek tlačítek, které poskytují přístup k operacím POS. Obvykle jsou zde umístěny operací, které nejsou specifické pro aktuální transakci. **Transakce obrazovky** -Transaction obrazovka je na hlavní obrazovce v POS pro zpracování transakce prodeje a objednávek. Na obrazovce transakce mohou být konfigurovány pomocí návrháře rozvržení obrazovky. **Výchozí úvodní obrazovce** -někteří maloobchodníci raději, že pokladník přejít přímo na obrazovce transakce po přihlášení. Výchozí nastavení obrazovky start umožňuje uživatelům nastavit pro každé rozvržení obrazovky.

### <a name="assignment"></a>Přiřazení

Rozložení obrazovky může být přiřazena na úrovni obchodu, rejstříku nebo uživatele. Přiřazení uživatele přepíše žurnálu a uložení přiřazení a přiřazení přepíše žurnálu přiřazení úložiště. V jednoduchém případě, kde všichni uživatelé použít stejné rozvržení bez ohledu na roli nebo rejstříku rozvržení obrazovky lze nastavit pouze v obchodě. V případech, kde některé registry nebo uživatelé vyžadují speciální rozložení lze jim přiřadit správným způsobem.

### <a name="layout-sizes"></a>Velikosti rozvržení

Tato funkce se týká pouze Dynamics 365 verzi operace 1611. Vzhledem k tomu, že v mnoha případech lze použít rozložení obrazovky napříč více velikosti obrazovky a řešení, uživatelé mohou konfigurovat jejich rozložení a obsah pro každého. Aplikaci Retail POS automaticky zvolí nejbližší velikost rozložení zařízení v době spuštění. Rozvržení obrazovky může také obsahovat konfigurace pro úplné a kompaktní zařízení. Tato konfigurace umožňuje uživateli přiřadit k jedné obrazovce rozložení, které budou fungovat v různých velikostech a prvků v úložišti. **Moderní POS - plný** -úplné rozložení jsou obvykle nejvhodnější pro větší zobrazení jako na monitory PC nebo tablety. Uživatelé mohou zvolit uživatelské rozhraní prvky, které zahrnují určení jejich velikosti a umístění a jejich podrobné vlastnosti konfigurace. Rozložení plně podporují konfigurace na výšku a na šířku. **Kompaktní moderní POS -** -kompaktní rozložení jsou obvykle nejvhodnější pro telefony a malé tablety. Možnosti návrhu jsou omezeny kompaktní zařízení. Uživatelé mohou konfigurovat sloupce a pole pro potvrzení a součty podokna.

### <a name="screen-layout-designer"></a>Návrhář rozložení obrazovky

Velikost každé rozložení v rámci rozvržení obrazovky musí být nakonfigurován pomocí návrháře rozvržení obrazovky. Návrhář umožňuje uživatelům určit a nakonfigurovat prvky uživatelského rozhraní na obrazovce transakce. Návrhář rozvržení obrazovky stáhnout, nainstalovat a spustit nejnovější verzi aplikace při každém přístupu uživatele pomocí ClickOnce. Zkontrolujte požadavky na prohlížeč pro použití ClickOnce – některých prohlížečů, například Chrome, vyžadují rozšíření. **Číselnou klávesnici** -číselnou klávesnici je hlavní vstup na obrazovce POS transakcí. Může být nakonfigurován na obrazovce zobrazit celý pad, který je ideální pro dotykovými obrazovkami, nebo pouze vstupní pole, které lze použít s fyzickou klávesnicí. Nastavení čísla pad jsou k dispozici v celé rozložení. V 365 Dynamics verzi operace 1611 kompaktní rozložení mají vždy plnou čísel z obrazovky transakcí k dispozici. **Souhrnný panel** - souhrnný panel lze konfigurovat v jedné nebo dvěma sloupci zobrazíte pole řádku počet, částka slevy, poplatky, souhrn a daně. V 365 Dynamics verzi operace 1611 kompaktní rozložení podporují pouze jeden souhrnný sloupec. **Příjem** -** ** příjem panel obsahuje prodejní řádky, řádky platby a doručení informace o produktech a službách, které jsou zpracovávány v POS. Uživatelé mohou určit sloupce, šířku a umístění. V kompaktní rozložení v Dynamics 365 verzi operace 1611 můžete také nakonfigurovat další informace, které se objeví v řádku v hlavní trať. **Karta zákazníka** - zobrazí karta zákazníka informace vztahující se k aktuálně přidružené k transakci zákazníka. Skrýt nebo zobrazit další informace lze konfigurovat na kartě zákazníka. **Ovládací prvek karta** - ovládacího prvku karta lze umístit do rozvržení obrazovky a další ovládací prvky, například čísel karty zákazníka nebo mřížek tlačítek mohou být umístěny uvnitř karty. Ovládací prvek karta je kontejner, který umožňuje uživatelům přizpůsobit více obsahu na obrazovce. Ovládací prvek karta je dostupná pouze pro celé rozložení. ** Obrazu **-lze použít ovládací prvek obrázek zobrazit na obrazovce transakce úložiště logo nebo jiný obrázek značky. Ovládací prvek Obrázek je dostupná pouze pro celé rozložení. **Doporučené produkty** - li nakonfigurován pro životní prostředí, doporučené produkty ovládací prvek bude zobrazovat návrhy týkající se produktu založené na strojovém učení. Doporučené produkty řízení je dostupná pouze pro úplné rozložení Dynamics 365 verzi operace 1611. ** Vlastní ovládací prvek **-vlastní ovládací prvek funguje jako vyhrazené místo v rozvržení obrazovky, aby uživatelé rezervovat místa pro vlastní obsah. Vlastní ovládací prvek je pouze k dispozici pro celé rozložení.

<a name="see-also"></a>Viz také
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)



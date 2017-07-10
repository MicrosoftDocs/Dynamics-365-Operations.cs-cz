---
title: "Konfigurace rozložení obrazovky pro POS"
description: "Toto téma obsahuje informace o rozložení obrazovky pro prostředí POS aplikace Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 9f7f46c1bae5bac6eefa0b8c70b079cab76aa8b6
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Konfigurace rozložení obrazovky pro POS

[!include[banner](includes/banner.md)]


Toto téma obsahuje informace o rozložení obrazovky pro prostředí POS aplikace Microsoft Dynamics 365 for Retail.

Uživatelské rozhraní Microsoft Dynamics 365 for Retail point of sale (POS) lze konfigurovat pomocí kombinace vizuálních profilů a rozložení obrazovky, přiřadit obchodům, registrům nebo uživatelům.

## <a name="visual-profile"></a>Vizuální profil
Vizuální profily jsou přiřazeny registrům a slouží k určení vizuálních prvků, které jsou specifické pro evidenci a sdílené mezi uživateli. Libovolný uživatel, který se přihlásí do rejstříku bude mít stejný motiv, barvy a obrázky. 

**Číslo profilu** -číslo profilu je jedinečný identifikátor pro vizuální profil. 

**Popis** -popis umožňuje zadat smysluplný název, který vám pomůže identifikovat správný profil pro danou situaci.

**Motiv** -uživatelé mohou zvolit mezi světlým nebo tmavým motivem aplikace. Tato nastavení ovlivňují barvu písma a pozadí v rámci aplikace.

**Barva zvýraznění** -barva zvýraznění v celém POS slouží k odlišení nebo zvýraznění některých vizuálních prvků, jako jsou dlaždice, příkazová tlačítka nebo hypertextové odkazy. Tyto prvky většinou slouží k provádění akcí.

**Barva záhlaví** -barva záhlaví umožňuje uživateli konfigurovat barvu záhlaví stránky pro vlastní potřeby prodejce. Tato funkce je k dispozici pouze v Dynamics 365 for Retail verze 1611.

**Pozadí přihlašování** -uživatelé mohou zadat obrázek pozadí pro přihlašovací obrazovku. Velikost obrázků na pozadí je třeba uchovávat co nejmenší, protože ukládání a načítání velkých souborů může mít vliv na chování a výkon aplikace.

**Pozadí aplikace** - POS může také použít obrázek jako pozadí v aplikaci místo plné barvy motivu. Stejně jako u přihlašovací pozadí byste měli uchovávat co nejmenší velikost souboru.

## <a name="screen-layouts"></a>Rozložení obrazovky
Konfigurace rozložení obrazovky určuje akce, obsah a umístění ovládacích prvků uživatelského rozhraní na úvodní obrazovce POS a obrazovce transakce. 

**Úvodní obrazovka** - ve většině případů je uvítací stránka taková, kterou uživatelé uvidí při prvním přihlášení do POS. Úvodní obrazovka může obsahovat obrázek značky a mřížky tlačítek, které poskytují přístup k operacím POS. Obvykle jsou zde umístěny operace, které nejsou specifické pro aktuální transakci. 

**Obrazovka Transakce** - obrazovka je na hlavní obrazovce v POS pro zpracování prodejních transakcí a objednávek. Obrazovku Transakce lze konfigurovat pomocí návrháře rozvržení obrazovky. 

**Výchozí úvodní obrazovka** -někteří maloobchodníci mají raději, když pokladník po přihlášení přejde přímo na obrazovku Transakce. Výchozí nastavení obrazovky Start umožňuje uživatelům nastavit tento postup pro každé rozvržení obrazovky.

### <a name="assignment"></a>Přiřazení

Rozložení obrazovky mohou být přiřazena na úrovni obchodu, rejstříku nebo uživatele. Přiřazení uživatele přepíše přiřazení registru a obchodu a přiřazení registru přepíše přiřazení obchodu. V jednoduchém případě, kde všichni uživatelé používají stejné rozvržení bez ohledu na registr nebo roli, lze rozvržení obrazovky nastavit pouze v obchodě. V případech, kde některé registry nebo uživatelé vyžadují speciální rozložení, jim je lze přiřadit správným způsobem.

### <a name="layout-sizes"></a>Velikosti rozvržení

Tato funkce je k dispozici pouze v Dynamics 365 for Retail verze 1611. Vzhledem k tomu, že v mnoha případech lze použít rozložení obrazovky napříč více velikostmi obrazovky a řešení, uživatelé mohou konfigurovat jejich rozložení a obsah pro každého. Aplikace Retail POS automaticky zvolí nejbližší velikost rozložení zařízení v době spuštění. Rozvržení obrazovky může také obsahovat konfigurace pro úplné a kompaktní zařízení. Tato konfigurace umožňuje uživateli přiřadit k jedné obrazovce rozložení, která budou fungovat v různých velikostech a formátech v úložišti. 

**Moderní POS - úplné** -úplná rozložení jsou obvykle nejvhodnější pro větší zobrazení jak na monitorech PC, tak v tabletech. Uživatelé mohou zvolit, které prvky uživatelského rozhraní budou zahrnuty, určit jejich velikost a nakonfigurovat jejich podrobné vlastnosti. Plná rozložení podporují konfigurace na výšku a na šířku. 

**Modern POS - kompaktní -** -kompaktní rozložení jsou obvykle nejvhodnější pro telefony a malé tablety. Možnosti návrhu jsou omezeny pro kompaktní zařízení. Uživatelé mohou konfigurovat sloupce a pole pro potvrzení a součty podokna.

### <a name="screen-layout-designer"></a>Návrhář rozložení obrazovky

Každá velikost rozložení v rámci rozložení obrazovky musí být nakonfigurováno pomocí návrháře rozvržení obrazovky. Návrhář umožňuje uživatelům určit a nakonfigurovat prvky uživatelského rozhraní na obrazovce transakce. Návrhář rozvržení obrazovky používá ClickOnce ke stažení, instalaci a spuštění nejnovější verze aplikace pokaždé, když k němu uživatel přistupuje. Zkontrolujte požadavky na prohlížeč pro použití ClickOnce – některé prohlížeče, například Chrome, vyžadují rozšíření. 

**Číselná klávesnice** - číselná klávesnice je hlavní vstup na obrazovce POS transakcí. Může být nakonfigurována tak, aby se zobrazovala na celé obrazovce, což je ideální pro dotykové obrazovky, nebo pouze pro vstupní pole, které lze použít s fyzickou klávesnicí. Nastavení číselné klávesnice jsou k dispozici v celém rozložení. V aplikaci Dynamics 365 for Retail verze 1611 mají kompaktní rozložení vždy plnou číselnou klávesnici dostupnou z obrazovky Transakce.

**Souhrnný panel** - souhrnný panel lze konfigurovat s jedním nebo dvěma sloupci k zobrazení polí, jako je počet řádků, částka slevy, poplatky, souhrn a daně. V aplikaci Dynamics 365 for Retail verze 1611 podporují kompaktní rozložení pouze jeden souhrnný sloupec. 

**Příjem** - Panel příjmu obsahuje prodejní řádky, řádky platby a doručení informace o produktech a službách, které jsou zpracovávány v POS. Uživatelé mohou určit sloupce, šířku a umístění. V kompaktních rozloženích aplikace Dynamics 365 for Retail verze 1611 můžete také nakonfigurovat další informace, které se objeví v řádku pod hlavním řádkem. 

**Karta zákazníka** - tato karta zobrazuje informace o zákazníkovi vztahující se k aktuálně přidružené k transakci zákazníka. Kartu zákazníka lze nakonfigurovat tak, aby zobrazovala nebo skrývala další informace. 

**Ovládací prvek karty** - ovládací prvek karty lze umístit do rozvržení obrazovky a dalších ovládacích prvků, jako je číselná klávesnice, karta zákazníka nebo tlačítka mřížky, která mohou být umístěna uvnitř karty. Ovládací prvek karty je kontejner, který umožňuje uživatelům přizpůsobit více obsahu na obrazovce. Ovládací prvek karty je dostupný pouze pro celá rozložení. 

**Obraz** - Tento ovládací prvek lze použít k zobrazení loga obchodu nebo jiného obrázku značky na obrazovce transakce. Ovládací prvek obrázku je dostupný pouze pro celá rozložení. 

**Doporučené produkty** - Je-li nakonfigurován pro prostředí, ovládací prvek pro doporučené produkty bude zobrazovat návrhy týkající se produktu založené na strojovém učení. Řízení doporučených produktů řízení je dostupné pouze pro úplné rozložení Dynamics 365 for Retail verze 1611. ** Vlastní ovládací prvek **- vlastní ovládací prvek funguje jako vyhrazené místo v rozvržení obrazovky, aby uživatelé mohli rezervovat místa pro vlastní obsah. Vlastní ovládací prvek je dostupný pouze pro celá rozložení.

<a name="see-also"></a>Viz také
--------

[Instalace návrháře rozložení Retail POS](install-pos-layout-designer.md)





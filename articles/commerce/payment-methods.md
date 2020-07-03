---
title: Metody platby
description: Každý typ platby, kterou prodejce přijímá, musí být nakonfigurován při nastavení systému. Tento článek popisuje typy plateb, které lze nastavit, a také proces jejich nastavení.
author: sericks007
manager: AnnBe
ms.date: 06/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 710c2f3bbe5b76af6d0bc0bf9a469e52c98c18d2
ms.sourcegitcommit: 550006e6376815237c21b5b30e928353f62fd97c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/18/2020
ms.locfileid: "3463153"
---
# <a name="payment-methods"></a>Metody platby

[!include [banner](includes/banner.md)]

Každý typ platby, kterou prodejce přijímá, musí být nakonfigurován při nastavení systému. Tento článek popisuje typy plateb, které lze nastavit, a také proces jejich nastavení.

Maloobchodní prodejci mohou přijímat různé typy plateb za výrobky a služby, které prodávají. I když jsou hotovostní platby nejčastěji používaným typem platby, maloobchodní prodejci mohou také přijímat platby ve formě šeků, karet, kuponů apod. Každý typ platby, kterou prodejce přijímá, musí být nakonfigurován při nastavení systému v aplikaci Dynamics 365 Commerce. Následující seznam popisuje každý typ platby, který lze nastavit:

- **Hotovost** – peníze v podobě fyzické měny, například bankovky a mince. Měnou může být měna společnosti nebo místní měna obchodu.
- **Šek** – převoditelný nástroj opravňující k výběru určité částky v určité měně z uvedené banky. Šek má obvykle platnost neomezeně nebo šest měsíců od data vystavení, pokud není určena jiná doba platnosti. Toto období závisí na tom, z jaké banky se šek vybírá. Existují různé druhy šeků, například šeky na jméno, šekové formuláře, šeky na doručitele, šeky na řad. Můžete nastavit šeky jako způsob platby pro každý obchod. Šeky lze přijímat v měně definované na úrovni společnosti nebo na úrovni obchodu. Musíte nastavit šeky jako způsob platby dříve, než budete moci jako platbu v obchodě přijímat šeky.
- **Měna** – hlavní forma plateb, které neprobíhají ve výchozí měně společnosti. Mince a bankovky jsou dvěma podobami měny. Metoda platby v měně představuje všechny používané měny. Než budete moci začít používat tento typ platby, musíte nastavit měny a určit údaje o směnném kurzu těchto měn.
- **Karta** – všechny typy karet, které se používají, například debetní a kreditní karty. Je vhodné vytvořit na úrovni organizace jeden způsob platby kartou, který bude představovat všechny druhy karet. Na úrovni obchodů pak nastavte způsob platby pro každou kartu nebo soubor karet, které by měly být zpracovány pomocí stejného nastavení. Abyste mohli v obchodě přijímat platby kartou, je třeba nastavit karty různých výrobců dostupné na trhu, tedy například debetní a kreditní karty.
- **Dobropis** – dobropisy, které jsou vydané nebo vyplacené na pokladních místech. Dobropis může mít formu kreditu nebo vratky a je vystaven na základě zpětného prodeje. Jsou-li dobropisy pouze z části vyplaceny, vystaví program na novou zůstatkovou částku nový dobropis. Nový dobropis má nové číslo. Dobropis lze použít pouze jednou a systém uchovává záznamy o všech použitých číslech. Záznam lze zobrazit na stránce **Tabulka dobropisů**. Zákazník si nemůže nechat vyplatit částku přesahující hodnotu dobropisu.
- **Dárkový poukaz** – dárkové poukazy vydané a vyplacené na pokladním místě. U dárkových poukazů není povolen přeplatek. Všechny dárkové karty by měly mít mapování čísel karet. 
- **Účet zákazníka** – platby, které lze účtovat na účet zákazníka přímo u pokladny v okamžiku prodeje. Tento způsob platby dále slouží ke shromažďování informací o prodeji nebo slevách pro určitého odběratele, když odběratel provede platbu pomocí jiného způsobu platby. V takovém případě je třeba nastavit informace o zákazníkovi.
- **Věrnostní body** – body, které zákazníci hromadí přes věrnostní programy. Pokud vytváříte věrnostní programy, mohou zákazníci získat body a pak uplatňovat různé způsoby. Například v některých věrnostních programech mohou odběratelé uplatnit věrnostní body ve formě slevy nebo je dokonce použít jako způsob platby.

K nastavení způsobů platby je třeba dokončit následující úlohy.

1. Nastavte platební metody pro organizaci. Vytvořte metody platby, které jsou přijímány v rámci celé organizace.
2. Vytvoření celoorganizačních typů karet a čísel karet. Budou-li přijímány kreditní nebo debetní karty, je třeba vytvořit jeden typ úhrady pro karty a poté vytvořit celoorganizační typy karet a čísla karet.
3. Nastavte platební metody obchodu. Přiřaďte způsoby plateb ke každému obchodu a poté zadejte konkrétní nastavení pro každý způsob platby.
4. Nastavte karetní platební metody pro obchody. Pro jakékoli metody platby kartou, které obchod přijímá, dokončete nastavení karty.

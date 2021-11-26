---
title: Způsoby platby
description: Každý typ platby, kterou prodejce přijímá, musí být nakonfigurován při nastavení systému. Tento článek popisuje typy plateb, které lze nastavit, a také proces jejich nastavení.
author: BrianShook
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0450dbaa37365705ca59fd2223c9d3866054c12a
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779563"
---
# <a name="payment-methods"></a>Způsoby platby

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

1. Nastavte způsoby platby pro organizaci. Vytvořte způsoby platby, které jsou přijímány v rámci celé organizace.
2. Vytvoření celoorganizačních typů karet a čísel karet. Budou-li přijímány kreditní nebo debetní karty, je třeba vytvořit jeden typ úhrady pro karty a poté vytvořit celoorganizační typy karet a čísla karet.
3. Nastavte způsoby platby obchodu. Přiřaďte způsoby plateb ke každému obchodu a poté zadejte konkrétní nastavení pro každý způsob platby.
4. Nastavte karetní způsoby platby pro obchody. U jakýchkoli způsobů plateb kartou, které obchod přijímá, dokončete nastavení karty.

## <a name="handle-change-tendering-for-payment-methods"></a>Zpracování úhrady vrácení hotovosti u platebních metod

Některé způsoby platby nepodporují přímou úhradu vrácení hotovosti, pokud jsou finanční prostředky splatné zpět zákazníkům během transakcí pokladního místa. K úhradě vrácení hotovosti lze použít pouze způsoby platby **Hotovost** a **Měna**. 

Chcete-li zpracovat případy, kdy je během transakce vyžadována úhrada vrácení hotovosti, ale platební metoda ji nepodporuje, můžete definovat způsob platby **Úhrada vrácení hotovosti**. Když pro obchod nastavujete způsoby platby obchodu, vyberte způsob, kterou chcete použít. Poté v oddíle **Změna** v poli **Úhrada vrácení hotovosti** zadejte způsob platby Úhrada vrácení hotovosti. Můžete například zadat **1** a tak vyjádřit, že hotovost lze použít jako možnost platby při úhradě vrácení hotovosti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Úloha vyčištění položek zásob na skladě v řízení skladu
description: Toto téma popisuje úlohu vyčištění položek, která pomáhá zlepšit výkon systému identifikací a odstraněním souvisejících, ale nepotřebných záznamů.
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 9d01c577fc33564d3517d242e9b01f73cc8e079c
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015934"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Úloha vyčištění položek zásob na skladě v řízení skladu

Výkon dotazů, které se používají k výpočtu zásob na skladě, je ovlivněn počtem záznamů v příslušných tabulkách. Jedním ze způsobů, jak zlepšit výkon, je snížení počtu záznamů, které musí databáze zvážit.

Toto téma popisuje úlohu vyčištění položek, která odstraní nepotřebné záznamy v tabulkách InventSum a WHSInventReserve. Tyto tabulky ukládají informace o množství na skladě pro položky, které jsou povoleny pro zpracování správy skladu. (Tyto položky se označují jako položky WHS.) Vymazání těchto záznamů může výrazně zlepšit výkon výpočtů na skladě.

## <a name="what-the-cleanup-job-does"></a>Co dělá úklidová práce

Úloha na vyčištění položek odstraní všechny záznamy v tabulkách WHSInventReserve a InventSum, kde jsou všechny hodnoty pole *0* (nula). Tyto záznamy mohou být odstraněny, protože nepřispívají k informacím na skladě. Úloha odstraní pouze záznamy, které jsou pod úrovní **Umístění**.

Je-li povolen negativní fyzický stav zásob, nemusí být úloha čištění schopna odstranit všechny relevantní položky. Důvodem tohoto omezení je, že úloha musí umožňovat zvláštní scénář, kde registrační značka má více sériových čísel a jedno z těchto sériových čísel je negativní. Například systém bude mít po ruce na úrovni registrační značky nulovou hodnotu, pokud bude mít registrační značk +1 ks sériového čísla 1 a –1 ks sériového čísla 2. U tohoto zvláštního scénáře úloha provede první odstranění, kde se nejprve pokusí odstranit z nižších úrovní.

## <a name="schedule-and-configure-the-cleanup-job"></a>Naplánujte a nakonfigurujte úlohu čištění

Úloha pro vyčištění položek na skladě je k dispozici na **Řízení zásob \> Periodické úkoly \> Čištění \> Vyčištění záznamů na skladě pro správu skladů**. Pomocí standardního nastavení úlohy můžete ovládat rozsah a plán spuštění úlohy. Kromě toho jsou k dispozici následující nastavení:

- **Vymazat, pokud nebylo aktualizováno po tento počet dní** - Zadejte minimální počet dní, po které by úloha měla počkat, než odstraní záznam na skladě, který klesl na nulové množství. Toto nastavení použijte, abyste snížili riziko odstranění dosud používaných položek. Pokud chcete provést čištění co nejdříve, zadejte buď *0* (nula) nebo nechte pole prázdné.
- **Maximální doba provedení (hodiny)** - Zadejte maximální dobu provedení úlohy čištění v hodinách. Pokud úloha není dokončena před uplynutím této doby, uloží práci, kterou doposud dokončila, a poté se uzavře. Tato schopnost je zvláště důležitá pro implementace, které mají vysoké využití zásob. V těchto případech byste měli naplánovat spuštění úlohy v době, kdy je zatížení systému co nejlehčí. Pokud chcete, aby dávková úloha pokračovala, dokud nebude dokončena, zadejte buď *0* (nula), nebo nechte pole prázdné. Toto nastavení je k dispozici, pouze pokud byla související funkce [zapnuta ve vašem systému](#max-execution-time).

I když můžete úlohu spustit v běžné pracovní době, doporučujeme ji spustit mimo pracovní dobu. Tímto způsobem pomáháte předcházet konfliktům, které mohou nastat, pokud uživatel pracuje se záznamem, který se právě čistí.

Pokud se úloha pokusí odstranit záznam pro položku, zatímco je tento záznam používán jiným uživatelem, dojde k chybě zablokování u úlohy vyčištění nebo uživatele.

Při spuštění úlohy má velikost potvrzení 100. Jinými slovy, bude se snažit potvrdit jednou za každých 100 vymazání. Protože jsou však některé výměny založeny na sadě, mohou existovat scénáře, ve kterých lze ve stejné transakci odstranit více než 100 záznamů. Proto může někdy dojít k eskalaci blokování.

## <a name="possible-user-impact"></a>Možný dopad na uživatele

Uživatelé mohou být ovlivněni, pokud úloha pro vyčištění položek odstraní všechny záznamy pro danou úroveň (například úroveň registrační značky). V tomto případě nemusí být funkce pro zjištění, zda byly zásoby dříve k dispozici na registrační značce, podle očekávání funkční, protože příslušné položky na skladě již nejsou k dispozici. (Tato funkce kontroluje stav **Množství \<\> 0** v nastavení **Zobrazení rozměrů** , když uživatelé zobrazují informace na skladě.) Nicméně zlepšení výkonu, které poskytuje úloha vyčištění, by mělo tuto malou ztrátu funkčnosti nahradit.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Zpřístupněte nastavení Maximální doba provedení

Ve výchozím nastavení není nastavení **Maximální doba provedení** dostupné. Pokud ji chcete použít, musíte použít [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) pro zapnutí související funkce ve vašem systému. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Maximální doba provedení pro úlohu čištění položek na skladě v rámci správy skladu*

--- 
title: "Nastavení ověření párování faktur závazků"
description: "Tento záznam používá ukázkovou společnost USMF."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8959cf3a45f42e0ef5f0d79726c63184c274efff
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Nastavení ověření párování faktur závazků

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento záznam používá ukázkovou společnost USMF. Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky. Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur. Pokud vaše právnická osoba sleduje výdaje, jako jsou například dopravné, pomocí nákladů, ujistěte se, že je vybrán konfigurační klíč Poplatky.  Párování faktur závazků je procesem párování informací na faktuře dodavatele, nákupní objednávce a příjemce produktu. Rozdíly mezi těmito dokumenty jsou označovány jako odlišnosti v párování. Odlišnosti v párování se porovnávají s odchylkami, které jsou zadány. Pokud odchylka párování překračuje procento nebo částku tolerance, zobrazí se odpovídající ikona ve formuláři Faktura dodavatele a ve formuláři Podrobnosti o párování faktur.

1. Přejděte do nabídky Závazky > Nastavení > Parametry závazků.
2. Klikněte na kartu Ověření faktury.
3. Zaškrtněte nebo zrušte zaškrtnutí políčka Povolit ověření párování faktur.
    * Vyberte, zda má být před zaúčtováním faktury obsahující odchylky párování faktur vyžadováno schválení. Pokud zde nastavíte Povolit s varováním, vizuální označení budou zobrazeny v případě, že odchylka při párování faktur bude vyšší než tolerance. I přesto však bude možné zaúčtovat fakturu. Pokud chcete použít workflow společně s ověřením párování faktur, ujistěte se, v poli Zaúčtovat fakturu s odchylkami je vybrána hodnota Povolit s varováním, abyste nemuseli proces schvalovat vícekrát.  
    * V poli Automaticky aktualizovat stav záhlaví faktury určete, zda se párování provede automaticky při zadání dat faktury pomocí systému. Doporučená nastaveny je hodnota Ano, pokud nemáte obavy o výkon vstupních dat. Zakázání automatických aktualizací umožní systému pracovat rychleji, protože ověřování párování faktur bude při zadávání dat vynecháno. Pokud je nastavena hodnota Ne, úředník pro zadání dat bude muset ručně aktualizovat stav párování faktury, aby mohl vidět výsledky ověření párování faktur.  
4. Přepněte rozšíření oddílu Párování součtu faktur.
5. Zaškrtněte nebo zrušte zaškrtnutí políčka Párování součtu faktur tak, aby skutečné součty faktur odpovídaly očekávaným součtům.
    * Určete, zda bude zobrazena ikona, je-li odchylka párování faktur vyšší než tolerance. Můžete vybrat zobrazení ikony, když je kladný rozdíl vyšší než tolerance nebo pokud kladný nebo záporný rozdíl je vyšší než tolerance.  
    * Například tolerance je 5 procent a celková částka faktury v nákupní objednávce je 100,00. Proto se bude ikona párování cen zobrazena, pokud celková částka faktury na faktuře překročí cenu 105,00. Pokud vyberete volbu Pokud vyšší nebo nižší než tolerance, bude ikona zobrazena také v případě, že částka faktury je nižší než 95,00.  
6. V poli Tolerance součtu faktur v procentech je třeba zadat číslo.
7. Přepněte rozšíření oddílu Párování ceny a množství.
    * V poli Zásady párování řádků vyberte hodnotu, která má být použita jako výchozí zásada pro právnickou osobu, se kterou pracujete. Možnost "Nevyžadovaná" znamená, že nejsou zapotřebí ověřování ceny na jednotlivých řádcích faktury podle ceny nákupní objednávky nebo množství na faktuře na dodacím listu. "Dvoucestné párování" znamená, že je požadováno ověřovací řádků faktury, ale při ověření jsou zahrnuty pouze nákupní objednávky a dokumenty s fakturou dodavatele. Příjemka produktu není promítnuta do ověření párování. "Třícestné párování" znamená, že čistá jednotková cena na faktuře se bude porovnávat s čistou jednotkovou cenou nákupní objednávky, a odpovídající množství v příjemce produktu se bude porovnávat s množstvím ve faktuře.  
    * Při použití zásady párování typu Dvoucestné párování nebo Třícestné párování, můžete nastavit procentuální hodnoty tolerance ceny pro právnickou osobu, položky a dodavatele na stránce Tolerance ceny položky. Při porovnání faktur dodavatelů s informacemi na nákupních objednávkách vyhledá se vhodná procentuální hodnota tolerance cen.  
8. Vyberte volbu v poli Zásady párování řádků.
    * Chcete-li povolit různé úrovně párování pro zboží, dodavatele, kombinaci dodavatele a zboží nebo řádek nákupní objednávky, vyberte hodnotu v poli Povolit přepsání zásad párování. Zásady párování řádku právnické osoby lze obejít pro určitého dodavatele, zboží nebo kombinaci dodavatele a zboží na stránce Zásady párování.  
    * Chcete-li spárovat celkové ceny pro řádkové položky na fakturách, vyberte hodnotu v poli Párování celkových cen. Tento typ párování je užitečný, když dodavatel odešle více faktur pro stejný řádek nákupní objednávky. Můžete porovnat informace o ceně pro čistou částku na každém řádku faktury a všechny čekající a dříve zaúčtované řádky faktury s čistou částkou na odpovídajícím řádku nákupní objednávky.  
9. V poli Párování celkových cen vyberte možnost.
10. V poli Tolerance celkové nákupní ceny je třeba zadat číslo.
11. Přepněte rozšíření oddílu Párování nákladů.
12. Aby odpovídaly skutečným nákladům s očekávanými náklady na základě informací o nákupní objednávce, zaškrtněte políčko Porovnání nákladů.
13. Zavřete stránku.



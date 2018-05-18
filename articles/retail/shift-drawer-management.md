---
title: "Řízení směny a zásuvky s hotovostí"
description: "Tento článek vysvětluje, jak nastavit a používat dva typy směn pro maloobchodní pokladní místo (POS) - sdílené a samostatné. Sdílené směny může používat více uživatelů na více místech, zatímco samostatné směny může využívat vždy pouze jeden pracovník najednou."
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: c1483d3240d266845cea7789b70c038cb98fdfcc
ms.contentlocale: cs-cz
ms.lasthandoff: 03/22/2018

---

# <a name="shift-and-cash-drawer-management"></a>Řízení směny a zásuvky s hotovostí

[!include [banner](includes/banner.md)]

Tento článek vysvětluje, jak nastavit a používat dva typy směn pro maloobchodní pokladní místo (POS) - sdílené a samostatné. Sdílené směny může používat více uživatelů na více místech, zatímco samostatné směny může využívat vždy pouze jeden pracovník najednou.

Existují dva typy směn pro maloobchodní pokladní místo (POS): samostatná a sdílená. Samostatné směny může používat vždy jen jeden pracovník najednou. Sdílené směny může využívat více uživatelů na více místech. Tím se prakticky vytvoří jedna směna pro více pracovníků v obchodě.

## <a name="standalone-shifts"></a>Samostatné směny
Samostatné směny se používají v případě tradičních, pevných pokladních míst, kde je hotovost odsouhlasena nezávisle pro každou pokladnu POS. Například v prostředí potravin se obvykle používá několik pevných pokladen POS, a pokladník je přiřazena ke každé z nich. V tomto případě každá pokladna pravděpodobně používá samostatnou směnu a pokladník je odpovědný za pokladní zásuvku nebo fyzickou hotovost v pokladně. Samostatné směny zahrnují všechny činnosti v dané pokladně během pracovní směny pokladníka. Aktivity mohou zahrnovat počáteční částku, která je uložena v pokladní zásuvce, veškerou odebranou a přidanou hotovost prostřednictvím operací, jako jsou například odvody od banky a plovoucí zůstatek, nebo výkaz úhrad na konci směny.

### <a name="set-up-a-stand-alone-shift"></a>Nastavení samostatné směny

Samostatná směna je určena na úrovni pokladní zásuvky. Tento postup vysvětluje, jak nastavit samostatnou směnu na pokladně POS.

1.  Klikněte na **Maloobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily PO** &gt; **Hardwarové profily**.
2.  Vyberte profil hardwaru použitý pro samostatnou směnu.
3.  Na pevné záložce **Zásuvka** potvrďte, že je možnost **Zásuvka sdílené směny** nastavena na **Ne**.
4.  Klikněte na možnost **Uložit**.
5.  Klikněte na tlačítko **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Pokladny**.
6.  Vyberte pokladu, která vyžaduje samostatnou směnu, a klepněte na tlačítko **Upravit**.
7.  V poli **Hardwarový profil** vyberte hardwarový profil, který jste vybrali v kroku 2.
8.  Klikněte na možnost **Uložit**.
9.  Klikněte na **Maloobchodní prodej** &gt; **Maloobchodní IT** &gt; **Distribuční plán**.
10. Vyberte distribuční plán **1090** a poté kliknutím na **Spustit nyní** synchronizujte změny v systému POS.

### <a name="use-a-stand-alone-shift"></a>Použití samostatné směny

1.  Přihlaste se k systému POS.
2.  Pokud není žádná směna otevřená, vyberte **Otevřít novou směnu**.
3.  Přejděte k operaci **Počáteční částka výkazu** a určete výši hotovosti přidanou do pokladní zásuvky na začátku pracovního dne.
4.  Proveďte nějaké transakce.
5.  Na konci dne vyberte **Deklarovat úhradu** a deklarujte hotovost, která zůstala v zásuvce s hotovostí.
6.  Zadejte pokladní hotovost a kliknutím na tlačítko **Uložit** uložte výkaz úhrad.
7.  Výběrem možnosti **Zavřít směnu** zavřete směnu.

**Poznámka:** v závislosti na používaných obchodních procesech jsou během směny k dispozici i další operace. Operace **Odvod do trezoru**, **Odvod do banky** a **Odstranění úhrady** lze použít k odebrání peněz z pokladní zásuvky během dne nebo před uzavřením směny. Pokud v pokladní zásuvce dochází hotovost, můžete použít operaci **Zadání plovoucího zůstatku** pro přidání hotovosti do pokladny.

## <a name="shared-shifts"></a>Sdílené směny
Sdílené směny se používají v prostředí, kde více pokladníků sdílí zásuvku s hotovostí nebo jejich sadu v průběhu pracovního dne. Sdílené směny se obvykle používají v prostředí s mobilním systémem POS. V mobilním prostředí není jednotlivý pokladník přiřazen a odpovědný za jednu zásuvku. Místo toho všichni pokladníci musí být schopni řídit prodej a přidat hotovost do jakékoliv zásuvky s hotovostí, která je jim nejblíže. V tomto scénáři jsou zásuvky s hotovostí sdílené mezi pokladníky součástí sdílené směny. Všechny zásuvky s hotovostí ve sdílených směnách jsou součástí téže směny pro účely aktivit, které se vztahují k řízení hotovosti pro danou směnu. Do počáteční částky pro směnu je proto vhodné zahrnout součet všech hotovostí ve všech zásuvkách s hotovostí, které jsou součástí sdílené směny. Stejně tak bude výkaz úhrad součet všech hotovostí ve všech zásuvkách s hotovostí, které jsou součástí sdílené směny. **Poznámka:** v každém obchodě je možné v každém okamžiku otevřít pouze jednu sdílenou směnu. Sdílené a samostatné směny lze použít ve stejném obchodě.

### <a name="set-up-a-shared-shift"></a>Nastavení sdílené směny

1.  Klikněte na **Maloobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily PO** &gt; **Hardwarové profily**.
2.  Vyberte profil hardwaru použitý pro sdílenou směnu.
3.  Na pevné záložce **Zásuvka** nastavte možnost **Zásuvka sdílené směny** na **Ano**.
4.  Klikněte na možnost **Uložit**.
5.  Klikněte na tlačítko **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Pokladny**.
6.  Vyberte pokladu, která vyžaduje sdílenou směnu, a klepněte na tlačítko **Upravit**.
7.  V poli **Hardwarový profil** vyberte hardwarový profil, který jste vybrali v kroku 2.
8.  Klikněte na možnost **Uložit**.
9.  Klikněte na **Maloobchodní prodej** &gt; **Maloobchodní IT** &gt; **Distribuční plán**.
10. Vyberte distribuční plán **1090** a poté kliknutím na **Spustit nyní** synchronizujte změny v systému POS.

### <a name="use-a-shared-shift"></a>Použití sdílené směny

1.  Přihlaste se k systému POS.
2.  Pokud systém POS není zatím připojen k hardwarové stanici, vyberte **Operace bez zásuvky** a potom výběrem operace **Vybrat hardwarovou stanici** nastavte hardwarovou stanici pro sdílenou směnu jako aktivní. Tento krok je nutný pouze při prvním přidání pokladny do prostředí sdílené směny.
3.  Odhlaste se ze systému POS a znovu se přihlaste.
4.  Vyberte **Vytvořit novou směnu**.
5.  Vyberte **Počáteční částka výkazu**.
6.  Zadejte počáteční objem ve všech zásuvkách s hotovostí v obchodě, které jsou součástí sdílené směny, a potom klepněte na tlačítko **Uložit**.
    -   Pokud chcete přidat součást počáteční částky z každé následné zásuvky s hotovostí, pomocí operace **Vybrat hardwarovou stanici** nastavte hardwarovou stanici jako aktivní.
    -   Chcete-li přidat konkrétní zásuvku s hotovostí, použijte operaci **Otevřít zásuvku**.
    -   Pokračujte, dokud všechny zásuvky ve sdílené směně nemají svůj podíl z počáteční částky.

7.  Na konci dne otevřete každou zásuvku s hotovostí a odeberte hotovost.
8.  Po odebrání hotovost z poslední zásuvky spočítejte veškerou hotovost ze všech zásuvek s hotovostí.
9.  Pomocí operace **Deklarovat úhradu** deklarujte celkovou výši hotovosti ze všech zásuvek s hotovostí, které jsou součástí sdílené směny.
10. Pomocí operace **Zavřít směnu** zavřete sdílenou směnu.

## <a name="shift-operations"></a>Operace směny
Chcete-li změnit stav směny nebo zvýšit či snížit množství peněz v zásuvce, lze provést různé akce. Níže uvedená část popisuje tyto operace směny pro Dynamics 365 for Retail Modern POS a Cloud POS.

**Otevřená směna**

POS vyžaduje, aby uživatel měl aktivní, otevřenou směnu, aby mohl provádět všechny operace, které by měly za následek finanční transakci, například prodej, vrácení nebo příkaz odběratele.  

Během přihlašování do POS systém nejprve zkontroluje, zda má uživatel k dispozici na aktuální registrační pokladně aktivní směnu. V opačném případě uživatel pak může otevřít novou směnu, pokračovat v existující směně nebo pokračovat v přihlašování v režimu "bez zásuvky" režim, v závislosti na konfiguraci systému a jejich oprávněních.

**Počáteční částka výkazu**

Tato operace je často první akcí, kterou provede nově otevřená směna. Uživatelé určují počáteční množství hotovosti v zásuvce pro směnu. To je důležité kvůli výpočtu přebytku/nedostatku, ke kterému dochází při uzavírání účtů směny pro tuto částku.

**Zadání plovoucího zůstatku**

Plovoucí položky jsou neprodejní transakce, které se provádějí v aktivní směně a které zvyšují částku v hotovosti v zásuvce. Typickým příkladem plovoucí položky je přidání další změny do zásuvky, když se vyčerpává paměť.

**Odstranění úhrady**

Odebrání úhrady jsou neprodejní transakce, které se provádějí v aktivní směně ke snížení částky v zásuvce s hotovostí. To se nejčastěji používá ve spojení s plovoucím zůstatkem na odlišné směně. Například registrace 1 dochází při změně, takže uživatel v registru 2 provede odebrání úhrady ke snížení množství v zásuvce. Uživatel na registrační pokladně 1 by potom provedl plovoucí zůstatek pro zvýšení částky.

**Pozastavit směnu**

Uživatelé mohou pozastavit své aktivní směny k uvolnění aktuální registrační pokladny pro jiného uživatele, nebo pro přesun své směny na jinou registrační pokladnu (to se často označuje jako plovoucí pokladna). 

Pozastavení směny zabraňuje všem novým transakcím a změnám směn až do obnovení.

**Obnovit směnu**

Tato operace umožňuje uživateli obnovit dříve pozastavenou směnu na registrační pokladně, která již nemá aktivní směnu.

**Výkaz úhrad**

Výkaz úhrad je akce, kterou uživatel provedne k určení celkové peněžní částky v zásuvce, nejčastěji před uzavřením směny. Jedná se o hodnotu, která se porovnává proti očekávané směně k výpočtu částky přebytku/nedostatku.

**Odvod do trezoru**

Odvody do trezoru lze provést kdykoli během aktivní směny. Tato operace odstraní peníze ze zásuvky, aby mohly být přeneseny na bezpečnější místo, jako je například trezor v zadní místnosti. Celková částka zaznamenaná pro odvody do trezoru je stále zahrnuta v součtech směny, ale není nutné ji počítat jako součást výkaz úhrad.

**Odvod do banky**

Odvody do banky jsou stejně jako odvody do trezoru prováděny na aktivních směnách. Tato operace odstraní peníze ze směny a připraví je na bankovní vklad.

**Zavřít směnu bez zadání částky**

Neurčené uzavřená směna je směna, která již není aktivní, ale ještě nebyla zcela uzavřena. Směny uzavřené bez zadání částky nelze obnovit jako pozastavené směny, ale postupy, jako jsou výkazy počátečních částek a výkazy úhrad lze provést později nebo z jiné registrační pokladny.

Směny uzavřené bez zadání částky se často používají k uvolnění registru pro nového uživatele nebo směnu, aniž by bylo nutné tuto směnu plně spočítat, odsouhlasit a zavřít. 

**Zavřít směnu**

Tato operace vypočítá součty směny, částky přebytku/nedostatku a potom dokončí aktivní nebo bez zadání částky uzavřenou směnu. Nelze obnovit nebo upravit uzavřené směny.  

**Spravovat směny**

Tato operace umožňuje uživatelům zobrazit všechny aktivní, pozastavené a bez zadání částky uzavřené směny obchodu. V závislosti na svých oprávněních mohou uživatelé provádět závěrečné uzávěrkových postupy, jako je výkaz úhrad a zavírání směn pro neurčené směny uzavřené bez zadání částky. Tato operace také umožní uživatelům zobrazit a odstranit neplatné směny ve vzácných případech, kdy je směna zanechána ve špatném stavu po přepnutí mezi režimy offline a online. Tyto neplatné směny neobsahují žádné finančních informace nebo transakční data potřebná pro vyrovnání. 


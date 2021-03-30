---
title: Řešení potíží s diskrétní výrobou
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s diskrétní výrobou.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2004a48455939855df54c3087a11c8003d825566
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222746"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Řešení potíží s diskrétní výrobou

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s diskrétní výrobou.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Zobrazuje se následující chybová zpráva: „Procesy správy skladu se aktuálně používají. Pokud řádky práce ještě nejsou zaregistrovány, můžete zrušit vytvořenou práci a jakékoli řádky vytížení nebo dodávky a poté pokračovat v procesu výdeje nebo dodávky.“

### <a name="issue-description"></a>Popis problému

K tomuto problému dochází, pokud se pokusíte rezervovat nebo uvolnit práci pro řádek, ale transakce zásob má stav *Vydáno*, což znamená, že materiál byl vydán.

### <a name="issue-resolution"></a>Řešení problému

Chcete-li opravit problém, postupujte podle jednoho z následujících kroků.

- Změňte stav výrobní zakázky zpět na *Odhadováno* nebo *Uvolněno*.
- Otevřete stránku s podrobnostmi pro příslušnou výrobní zakázku. V podokně akcí na kartě **Sklad** ve skupině **Zastavit** vyberte **Zastavit a zrušit výdej** pro zrušení výdeje všech vydaných transakcí. Poté vyberte **Odebrat zastavení** a zpracujte výrobní zakázku.

Zde je vysvětlení funkcí *Zrušit výdej* a *Zastavit*:

- **Zrušit výdej** - Tato funkce stornuje stav transakcí zásob u řádků kusovníku a řádků vzorců, které mají stav od *Vydáno* po *Na objednávce*. Po dokončení práce pro výdej surovin je stav řádků nastaven na *Vydáno*. Tento stav zabrání resetování výrobní zakázky do stavu *Vytvořeno*. V tomto případě můžete použít funkci *Zrušit výdej* pro stornování transakcí ze stavu *Vydáno* a poté resetujte výrobní zakázku do stavu *Vytvořeno*.
- **Zastavit** - Tato funkce nastavuje příznak **Zastaveno** na výrobní zakázce, aby se zabránilo jakékoli aktualizaci stavu objednávky. Příznak **Zastaveno** naleznete na záložce s náhledem **Sklad** stránky s podrobnostmi o výrobní zakázce.

> [!NOTE]
>
> - Tlačítka jsou viditelná, pouze když je vytvořena výrobní zakázka pro položky, které jsou povoleny pro procesy skladu.
> - Skupina **Zastavit** je viditelná pouze na kartě **Sklad** v podokně akcí na stránce podrobností výrobní zakázky. Není viditelná na záložce s náhledem **Sklad** stránky se seznamem **Výrobní zakázky**.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Po změně jména pracovníka v globálním adresáři se neaktualizuje odpovídající název zdroje.

### <a name="issue-description"></a>Popis problému

Pokud změníte jméno pracovníka v globálním adresáři, odpovídající název zdroje se v hlavní skupině neaktualizuje.

### <a name="issue-resolution"></a>Řešení problému

Tento scénář není momentálně podporován. Chcete-li problém vyřešit, musíte ručně aktualizovat jméno zdroje.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Když vytvořím novou výrobní zakázku, neobdržím následující zprávu: „Vložit aktivní verzi kusovníku a postupu?“

### <a name="issue-description"></a>Popis problému

Když vytvoříte novou výrobní zakázku, po zadání čísla položky jsou pole **Pracoviště** a **Sklad** automaticky nastavena na výchozí pracoviště a sklad, které jsou definovány na stránce **Výchozí nastavení objednávky** pro položku dokončeného zboží. Navíc se automaticky zadá číslo aktivního kusovníku a číslo postupu. Neobdržíte následující zprávu, která vás vyzve k zadání těchto hodnot:

> Vložit aktivní verzi pro kusovník a postup?

### <a name="issue-resolution"></a>Řešení problému

Pokud vyberete produkt, pro který jsou pracoviště a sklad definovány na stránce **Výchozí nastavení objednávky**, nebudete vyzváni k vložení čísel kusovníku a postupu. Zobrazí se výzva, pouze pokud tyto hodnoty nejsou pro vybraný produkt definovány.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Výrobní zakázky se nezobrazují na stránce Označení.

### <a name="issue-description"></a>Popis problému

Některé výrobní zakázky se nezobrazují na stránce **Označení**.

### <a name="issue-resolution"></a>Řešení problému

Produkty, které mají následující konfiguraci, nejsou k dispozici pro označení. Proto nebudou zobrazeny na stránce **Označení**:

- Produkty jsou definovány jako produkty typu *skutečná hmotnost*.
- Jsou povoleny pro pokročilé skladové procesy.
- Jsou nakonfigurovány tak, aby byly řízeny zásadou *Standardní cena*.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Když se pokusím ukončit výrobní zakázku, zobrazí se následující chybová zpráva: „Hodnota výpočtu kusovníku consumptionCost musí být při uvolnění ze zásob záporná.“

Tento problém byl opraven ve verzi 10.0.15.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Když se stav výrobní zakázky změní z Ohlášeno jako dokončené na Konec, zobrazí se následující chybové zprávy: „Konflikt aktualizace. Standardní náklady neodpovídají finanční hodnotě zásob po aktualizaci“ a „Ve funkci InventCostMovement.checkVariance došlo k kritické chybě.“

K tomuto problému dochází, protože podkladová data byla změněna jiným procesem. Proces se pokusí aktualizovat data až pětkrát. Pokud konflikt přetrvává i po pěti pokusech, zobrazí se následující chybové zprávy:

> Konflikt aktualizace. Standardní náklady neodpovídají finanční hodnotě zásob po aktualizaci.

> Ve funkci InventCostMovement.checkVariance došlo k kritické chybě.

Toto chování je záměrné. Chcete-li problém zmírnit, obnovte dávkovou úlohu. Mělo by to nakonec běžet.

Pokud dávková úloha po jejím obnovení nadále selhává, ověřte, zda přesnost zaokrouhlování výchozí měny hlavní knihy odpovídá zaokrouhlování použitému na hodnoty v tabulce InventSum. Pokud byla přesnost zaokrouhlení změněna na nevyhovující hodnotu, pravděpodobně ji musíte změnit zpět na vyhovující hodnotu. Vyhledejte **ModifiedDateTime**. V tomto případě hodnota obvykle ukazuje, že přesnost zaokrouhlování byla nedávno změněna.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Když uvolním do skladu, zobrazí se následující chybová zpráva: „Položku RM nelze plně rezervovat. Ujistěte se, že je k dispozici celé množství, nebo položky rezervujte ručně, pokud je pole Rezervace na řádku kusovníku nastaveno na Ručně nebo Spuštěno. Výrobní zakázku nebylo možné uvolnit do skladu, protože nebylo možné rezervovat některé materiály." Stav je však aktualizován na Uvolněno.

### <a name="issue-description"></a>Popis problému

Pokud nejsou všechny položky řádku kusovníku fyzicky dostupné, když je uvolněna výrobní zakázka, a zásada **Uvolnění do skladu** je nastavena na *Vyžadovat úplnou rezervaci* ve výrobní zakázce, zobrazí se následující chybová zpráva:

> Položku RM nelze plně rezervovat. Ujistěte se, že je k dispozici celé množství, nebo položky rezervujte ručně, pokud je pole Rezervace na řádku kusovníku nastaveno na Ručně nebo Spuštěno. Výrobní zakázku nebylo možné uvolnit do skladu, protože nebylo možné rezervovat některé materiály.

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné a funguje podle očekávání.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Když se pokusím ukončit výrobní zakázku a nahlásit ji jako dokončenou, zobrazí se následující chybová zpráva: „Celkové správné množství nahlášené jako dokončené pro výrobu bude %1. Zpětná vazba pro poslední operaci je 0.00 celkem."

### <a name="issue-description"></a>Popis problému

Při pokusu o zaúčtování deníku sestavy jako dokončené na výrobní zakázce se zobrazí následující chybová zpráva:

> Celkové množství zboží hlášené jako dokončené pro výrobu bude %1. Zpětná vazba pro poslední operaci je 0.00 celkem.

### <a name="possible-cause"></a>Možná příčina

K tomuto problému dochází, pokud množství, která byla zaúčtována v posledních operacích, byla nesprávná. Například pokud je zahájena výroba, ale množství, které musí být zahájeno, není přiděleno, bude deníku karet postupů zaúčtován bez řádků. Chcete-li potvrdit situaci, otevřete výrobní zakázku a poté v podokně akcí na kartě **Zobrazení** vyberte **Karta postupu**.

### <a name="workaround"></a>Alternativní řešení

Tento problém můžete vyřešit zaúčtováním dalších deníků pro operace, pro které deníky nebyly správně zaúčtovány. Restartujte výrobní zakázku a výběrem odešlete další deníky. Tato akce nespustí výrobní zakázku, ale zaúčtuje deníky. Karta postupu by pak měla zobrazit množství, která byla zaúčtována, a měli byste být schopni úspěšně ukončit výrobní zakázky.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Mohu nahlásit výrobní zakázku jako dokončenou, když nahlásím chybné množství, ale nikoliv, když nahlásím čas nebo množství materiálu?

Chybové množství na výrobní zakázce nelze nahlásit, pokud také nehlásíte správné množství. Tento scénář **není** podporován. Aktualizace hlášení jako dokončeného nakonec selže při pokusu o ukončení výrobní zakázky a zobrazí se následující chybová zpráva:

> Chybí množství dokončené výroby.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Mohu sledovat sériová čísla dokončeného zboží podle sériových čísel spotřebovaného zboží?

Sériová čísla dokončeného zboží nelze sledovat oproti sériovým číslům materiálu, který výrobní zakázka spotřebuje k výrobě dokončeného zboží. Tento scénář není momentálně podporován. Řešením je vytvořit výrobní zakázky pro množství 1.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
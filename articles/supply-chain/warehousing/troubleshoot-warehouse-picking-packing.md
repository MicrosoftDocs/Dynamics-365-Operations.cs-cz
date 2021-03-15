---
title: Poradce při potížích s výdejem a balením
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při výdeji a balení v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993921"
---
# <a name="troubleshoot-picking-and-packing"></a>Poradce při potížích s výdejem a balením

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při výdeji a balení v Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Zobrazí se následující chybová zpráva: „Umístění dimenze nemůže zůstat prázdné, pokud je nastaveno sériové číslo dimenze.“

### <a name="issue-description"></a>Popis problému

Tato chybová zpráva se zobrazí, pokud vytvoříte převodní příkaz pro sériovou položku pomocí skladu, který je povolen pro pokročilou správu skladu (WMS), a po dokončení práce se pokusíte potvrdit zásilku.

### <a name="issue-resolution"></a>Řešení problému

Pole **Výchozí skladové místo příjmu** je prázdné pro tranzitní sklad ze skladu. Chcete-li tento problém vyřešit, zadejte výchozí skladové místo příjmu v tranzitním skladu. Ujistěte se, že toto umístění je řízeno registrační značkou.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Zobrazuje se následující chybová zpráva: „Neplatná registrační značka.“

### <a name="issue-description"></a>Popis problému

Tato chybová zpráva se zobrazí v aplikaci skladu při skenování ID registrační značky.

### <a name="issue-resolution"></a>Řešení problému

Ujistěte se, že v tabulce registračních značek existuje ID registrační značky a že položky a množství na registrační značce jsou k dispozici (jinými slovy nejsou blokovány).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Zobrazuje se následující chybová zpráva: „Pole 'Hmotnost nákladu'(=-%1) může obsahovat pouze kladná čísla. Aktualizace byla zrušena."

### <a name="issue-description"></a>Popis problému

Tato chybová zpráva se zobrazí, pokud existuje otevřená práce při zpracování práce z umístění balení do přechodných skladových míst nebo z přechodných skladových míst do umístění překladiště.

### <a name="issue-resolution"></a>Řešení problému

Abyste tento problém vyřešili, přejděte na **Správa systému \> Pravidelné úkoly \> Databáze \> Kontrola konzistence** a spusťte proces pro **Kontrola konzistence hmotnosti nákladu skladu**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Zobrazuje se následující chybová zpráva: „Množství není platné pro jednotku %1.“

### <a name="issue-description"></a>Popis problému

Tato chybová zpráva se zobrazí, když se pokusíte provést a *rozdělený výdej* ve více dávkách.

### <a name="issue-resolution"></a>Řešení problému

Pracovník skladu musí používat proces *Krátkodobé vyskladnění* v aplikaci skladu. Pokud se snažíte o výdej více dávek ze stejného místa, můžete také použít možnost **Úplný** v aplikaci skladu.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Nemohu přesunout inventář na místo, kde se kontrolují registrační značky.

### <a name="issue-description"></a>Popis problému

Vydaná množství v nákladu nelze snížit.

### <a name="issue-resolution"></a>Řešení problému

V předchozích verzích vyskladněné množství v nákladu nelze snížit. Nyní však můžete zrušit výdej v umístění, kde se kontroluje registrační značka. Musíte zadat hodnotu **Umístění** i hodnotu **Registrační značka** pro řádek nákladu na stránce **Snižte vydané množství**.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Mohu vytisknout poznámku k dodání nebo balicí obsah podle skladu?

### <a name="issue-description"></a>Popis problému

Chcete vytisknout poznámku k dodání nebo balicí obsah podle skladu nebo místa na stránce **Aktualizace řádku šablony pracovního auditu**.

### <a name="issue-resolution"></a>Řešení problému

Když tisknete dokument pomocí nastavení správy tisku, omezte rozsah (místo / sklad) prostřednictvím správy tisku místo výběru **Upravit nastavení tisku** na stránce **Aktualizace řádku šablony pracovního auditu**.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Po zaúčtování z prodejní objednávky nemůžu zrušit dodací list.

### <a name="issue-description"></a>Popis problému

Když jsou pro WMS povoleny procesy výdeje a expedice, nemůžete zrušit dodací list poté, co je zaúčtován z prodejní objednávky.

### <a name="issue-resolution"></a>Řešení problému

Chcete-li opravit zaúčtované dodací listy pro položky, které jsou povoleny pro WMS, musíte zaúčtování provést z nákladu, nikoli přímo z objednávky. Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. Obecně platí, že u prodejní objednávky, která byla vybrána a odeslána prostřednictvím procesů správy skladu, může být dodací list aktualizován z nákladu nebo dodávky a samotného dokladu prodejní objednávky. Pokud však u prodejní objednávky aktualizujete dodací list z dokladu prodejní objednávky, nelze přesto z nákladu nebo prodejní objednávky provést změnu dodacího listu. Proto doporučujeme použít zaúčtování dodacího listu z nákladu. V takovém případě bude povolen reverz, který musí být proveden z nákladu.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Zobrazí se mi následující chybová zpráva: "Pro seskupení nelze najít dostatek práce."

### <a name="issue-description"></a>Popis problému

Když používáte proces *Systémově řízený výdej seskupení*, pokud nakonfigurujete profil seskupení, kde lze vybrat například 10 pozic, proces funguje podle plánu, když je dostatek práce k výdeji do 10 pozic. Pokud však můžete vybrat pouze osm pozic, zobrazí se tato chybová zpráva, protože pro jedno seskupení není dostatek práce.

### <a name="issue-resolution"></a>Řešení problému

Chcete-li tento problém vyřešit, upravte profil seskupení a nastavte možnost **Aktivovat pozice** na *Ne*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
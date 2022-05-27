---
title: Podpora a obnovení
description: Toto téma vysvětluje, jak nastavit a používat proces podpory a obnovy u prodejních objednávek k vytvoření plánu fakturace pro položky obnovy.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 7de74f2b12e8e7201663ba78d936131b301b1ff9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685763"
---
# <a name="support-and-renewals"></a>Podpora a obnovení 

Toto téma vysvětluje, jak zadávat položky podpory nebo položky obnovy při zadávání prodejních objednávek. Tyto položky se používají k výpočtu částky poplatku za původní smlouvu o podpoře a/nebo částky za obnovení, která se používá při vytváření rozvrhu účtování ve fakturaci předplatného. Vaše společnost například prodá server zákazníkovi a vy nabízíte předplatné zálohování dat na první rok a možnost toto předplatné každý rok obnovovat. *Podpůrná položka* je předplatné na první rok a *obnovovací položka* je obnova pro každý následující rok.

Můžete zadat informace pro smlouvu o podpoře, smlouvu o obnovení nebo obojí. Když zadáte informace o smlouvě podpory, do prodejní objednávky se přidá pouze položka podpory. Když zadáte informace o smlouvě o obnovení, položka obnovení se použije k vytvoření rozvrhu účtování.

## <a name="support-and-renewal-setup"></a>Nastavení podpory a obnovení

Na stránce **Úrovně podpory a obnovy** můžete nastavit různé úrovně podpory pro položky podpory a obnovení. Podpora nebo obnovení může být procento z původní částky položky, nebo to může být standardní částka.

Výchozí úrovně podpory můžete vybrat na stránce **Parametry opakované fakturace smlouvy**.

Společnost může například nabízet následující úrovně podpory a obnovení.

| Úroveň podpory | Procento podpory | Procento obnovení |
|---|---|---|
| Neomezeno | 40 % | 30 % |
| Zlato | 25 % | 18% |
| Stříbro | 20 % | 14% |
| Bronz | 15% | 10 % |

Při vytváření úrovně podpory nebo prodloužení postupujte takto.

1. Na stránce **Úrovně podpory a prodloužení** vyberte **Nový**.
2. Do pole **Úroveň podpory** zadejte jedinečný název.
3. Zadejte popis do pole **Popis**.
4. V poli **Metoda výpočtu podpory** vyberte způsob výpočtu podpory. Pokud vyberete **Procenta**, zadejte procenta podpory do pole **Procento podpory**.
5. V poli **Metoda výpočtu prodloužení** vyberte způsob výpočtu prodloužení. Pokud vyberete **Procenta**, zadejte procenta prodloužení do pole **Procento prodloužení**.
6. Zvolte možnost **Uložit**.

### <a name="fields"></a>Pole

Stránka **Úrovně podpory a prodloužení** obsahuje následující pole.

| Pole | Popis |
|---|---|
| Úroveň podpory | Jedinečný identifikátor pro úroveň podpory nebo prodloužení (např. **Zlato** nebo **Stříbro**). |
| Popis | Popis úrovně podpory nebo prodloužení. |
| Metoda výpočtu podpory | Vyberte způsob výpočtu podpory pro úroveň: **Procenta** nebo **Standardní částka**. |
| Procento podpory | Pokud jste vybrali **Procenta** jako metodu výpočtu podpory, zadejte procento, které se použije k výpočtu ceny položky podpory. Pokud jste vybrali **Standardní částka** jako metoda výpočtu, částka je uvedena při vytvoření transakce. |
| Metoda výpočtu obnovení | Vyberte způsob výpočtu prodloužení pro úroveň: **Procenta** nebo **Standardní částka**. |
| Procento obnovení | Pokud jste vybrali **Procenta** jako metodu výpočtu prodloužení, zadejte procento, které se použije k výpočtu ceny položky prodloužení. Pokud jste vybrali **Standardní částka** jako metoda výpočtu, částka je uvedena při vytvoření transakce. |

## <a name="support-and-renewal-process"></a>Proces podpory a obnovení

Funkce podpory a prodloužení může u položek použít různé úrovně podpory a aktualizovat informace o prodloužení ve fakturaci předplatného.

Před použitím funkce podpory a prodloužení je třeba provést následující úlohy.

1. Na stránce **Úrovně podpory a prodloužení** vytvořte alespoň jednu úroveň podpory nebo prodloužení.
2. Na stránce **Nastavení položky** přidružte položku k položce podpory a prodloužení. Tato úloha je vyžadována pouze v případě, že chcete nastavit výchozí hodnoty pro položky podpory a/nebo prodloužení.
3. Na stránce **Parametry opakované fakturace smlouvy** zadejte výchozí nastavení podpory a prodloužení pro nové plány fakturace.

Chcete-li na položky použít různé úrovně podpory a aktualizovat informace o prodloužení, postupujte takto.

1. Na stránce **Všechny prodejní objednávky** vytvořte prodejní objednávku.
2. Na pevné záložce **Řádky proejní objednávky** vyberte položku.
3. Na kartě **Faktura** vyberte **Podpora a prodloužení \> Přidejte podporu a prodloužení**.
4. Na stránce **Proces podpory a prodloužení** sekce hlavičky se aktualizuje o nastavení ze stránky **Parametry opakované fakturace smlouvy**. Tyto hodnoty platí pro všechny položky podpory a prodloužení. (Pokud je například frekvence účtování nastavena na **Každoročně**, všechny vytvořené prodejní řádky, které mají položku prodloužení, mají roční frekvenci.) Chcete-li prodejní objednávku přidružit k existujícímu rozvrhu fakturace, vyberte hodnotu v poli **Číslo fakturačního plánu**.
5. Chcete-li změnit datum zahájení podpory nebo prodloužení, nastavte možnost **Přepsat datum zahájení** na **Ano**.
6. Chcete-li přidat nebo upravit položku podpory, vyberte zaškrtávací políčko **Podpora** a poté zadejte položku podpory do pole **Položka podpory**. Tato položka je přidána na prodejní objednávku.
7. Chcete-li přidat nebo upravit položku prodloužení, vyberte zaškrtávací políčko **Prodloužení** a poté zadejte položku prodloužení do pole **Položka prodloužení**. Když je prodejní objednávka fakturována, vytvoří se plán fakturace, který zahrnuje položku.
8. Vyberte **OK**.
9. Na kartě **Generovat** vyberte **Fakturu**. Po zaúčtování prodejní objednávky se vytvoří plán účtování. V podrobnostech zprávy se zobrazí oznámení, které obsahuje informace o plánu fakturace.
10. Na stránce seznamu **Všechny nebo aktivní plány fakturace** vyberte číslo plánu fakturace, jehož zkontrolovali podrobnosti na straně **Plány fakturace**.
11. Na pevné záložce **Řádky plánu fakturace** vyberte **Podpora a prodloužení** pro kontrolu podrobností o řádcích, které byly vytvořeny.

> [!NOTE]
> Pokud je nutné změnit počáteční datum prodloužení pro řádek plánu fakturace, můžete upravit hodnotu **Datum zahájení** pro řádek na stránce **Plány fakturace**. Když otevřete stránku **Zobrazit detail fakturace** pro řádek, pole **Datum zahájení fakturace** se aktualizuje o nové datum. Hodnota **Datum ukončení fakturace** se přepočítá na základě frekvence fakturace. Datum zahájení prodloužení lze aktualizovat pouze v případě, že nebyla vytvořena a zaúčtována první faktura za plán fakturace prodloužení. Po vytvoření a zaúčtování první faktury nelze datum zahájení upravit.

Proces podpory a prodloužení je dostupný pouze pro prodejní objednávku. Když přidáte položky podpory a prodloužení do prodejní objednávky, můžete vytvořit nový plán účtování nebo přidat položku prodloužení do existujícího plánu fakturace.

## <a name="support-and-renewal-audit"></a>Audit podpory a obnovení

Na stránce **Audit podpory a prodloužení** si můžete prohlédnout podrobnosti řádků plánu fakturace, které jsou vytvořeny z položky prodloužení v prodejní objednávce. Tato možnost je k dispozici pouze v případě, že je řádková položka plánu fakturace položkou prodloužení.

Chcete-li upravit informace o podpoře a prodloužení pro řádek plánu fakturace, postupujte takto.

1. Na stránce **Všechny plány fakturace** vyberte číslo plánu fakturace.
2. V sekci **Řádky plánu fakturace** vyberte řádek, který chcete odstranit, a poté vyberte **Podpora a prodloužení**.
3. Zkontrolujte všechny informace o položce podpory nebo prodloužení.
4. Proveďte požadované změny úrovně podpory nebo procenta nebo částky prodloužení a poté zadejte hodnotu do pole **Důvod pro změnu**.
5. Vyberte možnost **Proces**.

### <a name="fields"></a>Pole

Stránka **Audit podpory a prodloužení** obsahuje následující pole.

| Pole | Popis |
|-------|-------------|
| Číslo položky | Číslo položky pro řádek plánu fakturace. |
| Název produktu | Název produktu. |
| Úroveň plánu podpory | Zobrazte nebo změňte úroveň podpory pro položku prodloužení. |
| Procento obnovení | Zadejte procento prodloužení, které se použije při výpočtu jednotkové ceny pro položku prodloužení v rozvrhu fakturace. |
| Částka obnovení | Zadejte částku prodloužení, které se použije při výpočtu jednotkové ceny pro položku prodloužení v rozvrhu fakturace. |
| Důvod změny | Zadejte důvod změny informací o podpoře a prodloužení. Musíte zadat důvod při změně hodnot **Procento prodloužení**, **Částka prodloužení** nebo **Úroveň plánu podpory**. |
| Původní prodejní položka | Původní číslo prodejní položky z prodejní objednávky. |
| Původní čistá částka | Původní čistá částka za položku. |
| Původní úroveň podpory | Původní úroveň podpory za položku. |
| Původní procento obnovení | Původní procento prodloužení za položku. |
| Původní částka obnovení | Původní částka prodloužení za položku. |
| **Mřížka** | |
| Původní úroveň podpory | Předchozí úroveň podpory. |
| Původní procento obnovení | Procento předchozího prodloužení. |
| Původní částka obnovení | Částrka předchozího prodloužení. |
| Změnil/a | Jméno uživatele, který změnu provedl. |
| Datum a čas úpravy | Datum, kdy došlo ke změně. |
| Důvod | Důvod změny. |

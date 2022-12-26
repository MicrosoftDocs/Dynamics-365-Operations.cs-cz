---
title: Nevyrovnaná měna vykazování při spuštění roční uzávěrky
description: Tento článek vysvětluje, jak může být měna vykazování nevyrovnaná při spuštění uzávěrky na konci roku.
author: kweekley
ms.date: 12/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 31f79791330e076d4fbd7b604ba9f9c6cd9b9195
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850255"
---
# <a name="reporting-currency-out-of-balance-when-the-year-end-close-is-run"></a>Nevyrovnaná měna vykazování při spuštění roční uzávěrky

Po povolení funkce **Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku** (funkce **Sledování**) transakce hlavní knihy, které byly vyrovnány, již nebudou zahrnuty do počátečního zůstatku příštího fiskálního roku při spuštění uzávěrky hlavní knihy na konci roku. Vyloučení transakcí z hlavní knihy, které jsou vyrovnány, může pro zákazníky představovat problém při roční uzávěrce, pokud je pro hlavní knihu definována měna vykazování.

Vyrovnání hlavní knihy se provádí pouze pro zúčtovací měnu. Při vyrovnání transakcí v hlavní knize ověření pouze potvrdí, že se debety v zúčtovací měně rovnají kreditům ve zúčtovací měně. Částky v měně vykazování pro tyto transakce v hlavní knize nejsou ověřeny a debety se nemusí rovnat jejich kreditům. Kromě toho se při vyrovnání v hlavní knize automaticky nevypočítá a nezaúčtuje zisk/ztráta v měně vykazování.

Vzhledem k těmto omezením musí transakce zisku/ztráty při vyrovnávání hlavní knihy existovat v měně vykazování. Pokud není zisk/ztráta zahrnuta do vyrovnání hlavní knihy, výsledkem spuštění roční uzávěrky bude zpráva o nevyrovnání.

Následující příklad popisuje kroky k vyřešení tohoto problému před spuštěním uzávěrky na konci roku.

## <a name="example-setup"></a>Příklad nastavení

Chcete-li nastavit tento příklad, povolte funkci **Sledování** a nastavte hlavní účet 110180 na vyrovnání hlavní knihy. Následující obrázek ukazuje transakce hlavní knihy, které byly zaúčtovány pro právnickou osobu DEMF. Zúčtovací měna pro DEMF jsou americké dolary (USD) a měnou vykazování je euro (EUR).

![Transakce hlavní knihy v měně vykazování.](./media/reporting-currency-1.png)

Stránka **Vyrovnání hlavní knihy** zobrazuje transakce hlavní knihy pro hlavní účet 110180. Vyberte a podržte (nebo klikněte pravým tlačítkem) v mřížce a poté vyberte **Vložit sloupce**. Přidejte sloupec **Částka v měně vykazování**, aby byly zobrazeny všechny částky v měně transakce, zúčtovací měně a měně vykazování.

![Částka ve sloupci měny vykazování přidaná na stránku Vyrovnání hlavní knihy.](./media/Ledger-settlement2.png)

První dvě transakce hlavní knihy za 100 EUR jsou vyrovnány jako jedna skupina a další dvě transakce hlavní knihy za 200 EUR jsou vyrovnány jako další skupina. (Tyto dvě transakce budou mít různá ID vyrovnání.) Toto nastavení ukazuje, že organizace budou mít více skupin transakcí hlavní knihy, které jsou vyrovnány v různých časech a mají různá data vyrovnání. Po dokončení vyrovnání se na stránce **Vyrovnání hlavní knihy** zobrazí následující informace, když je filtrována tak, aby zobrazovala transakce, které mají stav **Vyrovnáno**.

![Vyrovnané transakce na stránce vyrovnání hlavní knihy.](./media/Settled-trans-filtered3.png)

Na stránce **Vyrovnání hlavní knihy** vyberte a podržte (nebo klikněte pravým tlačítkem) ve sloupci **Částka** a pak vyberte **Sečíst tento sloupec**. Tento krok opakujte pro sloupce **Částka v měně vykazování**. Zúčtovací měna musí mít rozdíl 0 (nula), aby došlo k vyrovnání. Neexistuje však žádné ověření částky vyrovnání pro měnu vykazování. Následující obrázek ukazuje rozdíl -27,79 USD pro měnu vykazování.

![Rozdíl v měně vykazování.](./media/Difference4.png)

## <a name="year-end-close"></a>Roční uzávěrka

Pokud je nyní spuštěna uzávěrka pro rok 2022, proces skončí chybovou zprávou o nevyrovnání. Tato chyba je přímo způsobena skutečností, že měna vykazování nemá částku vyrovnání hlavní knihy, která se rovná 0 (nule).

![Chybová zpráva, která označuje, že částka vyrovnání hlavní knihy není 0 (nula).](./media/YEC5.png)

## <a name="posting-reporting-currency-gainloss"></a>Zaúčtování zisku/ztráty měny vykazování

Aby uzávěrka proběhla úspěšně, musí být rozdíl v částce vykazované měny zaúčtován, obvykle jako zisk nebo ztráta, a zahrnut do vyrovnání hlavní knihy. Zisk/ztrátu měny vykazování lze zaúčtovat několika způsoby:

- Pokud jsou hlavním účtem závazky nebo pohledávky, vyrovnání těchto dokumentů vygeneruje požadovaný zisk/ztrátu. Tento účetní záznam musí být zahrnut do vyrovnání hlavní knihy, když jsou vyrovnány odpovídající transakce hlavní knihy z faktury, plateb, dobropisů atd.
- Pokud je hlavním účtem jakýkoli účet kromě účtu závazků nebo pohledávek, musí být zisk/ztráta zadán ručně. Když je zisk/ztráta zaúčtována, úroveň podrobnosti účetního záznamu je určena vaší organizací.
- Pro každý hlavní účet určete částku zisku/ztráty měny vykazování, které musí být zaúčtovány.

Jak bylo popsáno dříve, toto zaúčtování lze provést na stránce **Vyrovnání hlavní knihy**.

1. Filtrujte podle rozsahu dat, pro který chcete zaúčtovat zisk/ztrátu. Pokud plánujete zaúčtovat zisk/ztrátu za každý měsíc, filtrujte podle měsíce. Pokud plánujete zaúčtovat zisk/ztrátu za fiskální rok, filtrujte podle celého roku.
2. Filtrujte hlavní účet.
3. Filtrujte podle stavu tak, aby byly zobrazeny pouze transakce **Vyrovnáno**.
4. Přidejte celkovou částku do sloupce **Částka v měně vykazování**.
5. Pokud chcete zisk/ztrátu zaúčtovat na podrobnější úrovni, můžete provést další filtrování podle ID vyrovnání, finančních dimenzí atd. Celková částka ve sloupci **Částka v měně vykazování** představuje částku, pro kterou bude zaúčtován zisk/ztráta.
6. Přejděte do nabídky **Hlavní kniha \> Položky deníku \> Deníky úprav měny vykazování**.
7. Zadejte transakci pro zisk/ztrátu. Tento deník zaúčtuje úpravu pouze v měně vykazování. Částky v měně transakce a účetní měně, které jsou zaúčtovány, jsou vždy 0 (nula). Pokud se tento deník dosud nepoužíval, možná budete muset vytvořit název deníku, který má typ **Úprava měny vykazování** v nabídce **Obecná hlavní kniha \> Nastavení deníku \> Názvy deníků**.
8. Tato úprava nebude zaúčtována, pokud hlavní účet neumožňuje ruční zadání. Proto možná budete muset dočasně vypnout parametr **Nepovolit ruční zadávání** na stránce **Hlavní účet**.

![Ruční zadání na stránce dokladu deníku.](./media/Manual-entry6.png)

Po zaúčtování deníku úprav se vraťte na stránku **Vyrovnání hlavní knihy** a vyberte hlavní účet, pro který jste zaúčtovali zisk/ztrátu. Úprava zisku/ztráty musí být zahrnuta do vyrovnání hlavní knihy. Protože částka v měně vykazování nemusí být čistá 0 (nula), můžete zrušit vyrovnání všech předchozích transakcí a poté je znovu vyrovnat, ale tentokrát zahrňte zisk/ztrátu. Jak přesní chcete být při zaúčtování zisku/ztráty a vyrovnání tohoto zisku/ztráty ve vyrovnáních hlavní knihy záleží na vaší organizaci.

Následující obrázek ukazuje, že transakce pro 200 EUR nebyly vyrovnány a poté znovu označeny k vyrovnání. Tentokrát budou zahrnovat úpravu zisku/ztráty.

![Úprava zisku/ztráty na stránce Vyrovnání hlavní knihy.](./media/gain-loss7.png)

Po vyrovnání transakcí změňte filtr **Stav** tak, aby se na stránce zobrazovaly transakce **Vyrovnáno** . Součet ve sloupci **Částka v měně vykazování** je nyní 0 (nula). Uzávěrku lze nyní úspěšně spustit.

![Úspěšné uzavření roku.](./media/Zero-settled8.png)

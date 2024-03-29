---
title: Import směnných kurzů měn
description: Tento článek obsahuje informace o požadavcích na import směnných kurzů pro cizí měnu, které jsou publikovány poskytovatelům směnného kurzu.
author: EvgenyPopovMBS
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 27f9b06646d9ce948a6b4528c38c5df9784b24b2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894928"
---
# <a name="import-currency-exchange-rates"></a>Importovat směnné kurzy měn

[!include [banner](../includes/banner.md)]

Jestliže právnická osoba obdržela faktury v cizí měně, je nutné převést cizí měnu na místní měnu. To znamená, že jsou potřeba aktuální směnné kurzy pro různé měny. Tento článek obsahuje přehled požadovaných nastavení a zpracování nezbytných pro import referenčních směnných kurzů publikovaných prostřednictvím Internetu poskytovateli směnných kurzů, jako je Evropská centrální banka a centrální banky Ruska.

V následujících částech je popsán celkový tok informací, které se používají k nastavení a zpracování importu cizích směnných kurzů.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurace poskytovatele směnných kurzů
Než bude možné importovat směnné kurzy, musíte nastavit informace vyžadované zprostředkovateli, kteří nabízejí směnné kurzy. Pomocí stránky **Konfigurace zprostředkovatelů směnného kurzu** vyberte poskytovatele směnných kurzů. Někteří poskytovatelé směnných kurzů jsou zahrnuti v demo datech aplikace Dynamics 365 Finance. Ovládací prvky tohoto formuláře jsou popsány na následující stránce.

| Pole | popis                   |
|-----------|-----------------------------------|
| **Název**  | Název poskytovatele směnného kurzu.                                                                                                                                                                                     |
| **Klíč**   | Jedinečný identifikátor součásti všech konfiguračních informací požadovaný poskytovatelem. Tyto údaje jsou automaticky přidány pro každého poskytovatele směnného kurzu, kterého přidáte. |
| **Value** | Informace pro každý klíč. Tyto údaje jsou přidány pro každého poskytovatele směnného kurzu, kterého přidáte.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importovat směnné kurzy měn
Směnné kurzy můžete importovat ze zdroje poskytovatelů směnných kurzů a přidat je na stránce **Směnné kurzy měn**. Použijte stránku **Importovat směnné kurzy měn**, chcete-li importovat směnné kurzy. Následující tabulka obsahuje popis polí požadovaných k dokončení procesu importu.

| Pole | popis                   |
|-----------|-----------------------------------|
| **Typ směnného kurzu**                 | Typ směnného kurzu.                                                                                                                                                                                                                                                                                                                                                      |
| **Poskytovatel směnného kurzu**             | Poskytovatel směnného kurzu.                                                                                                                                                                                                                                                                                                                                                  |
| **Importovat jako**                       | Tento parametr řídí, zda mají být importovány k aktuálnímu datu nebo zadanému období. Pokud chcete použít rozsah dat, zadejte nebo vyberte počáteční a koncové datum.                                                                                                                                                                                                                |
| **Vytvořit nezbytné páry měn**    | Toto zaškrtávací políčko řídí automatické vytváření dvojic měn, pokud neexistují páry měn, které jsou importovány. Tato možnost nemusí být k dispozici pro některé poskytovatele.                                                                                                                                                                                               |
| **Přepsat existující směnné kurzy**   | Toto zaškrtávací políčko spravuje aktualizace stávajícího směnného kurzu pro dvojici měn, když směnný kurz k určitému datu již existuje. Pokud toto políčko nezaškrtnete, směnný kurz pro konkrétní data není importován, pokud již existuje jiný směnný kurz.                                                                                       |
| **Zabránit importu v den státního svátku** | Toto zaškrtávací políčko řídí import směnného kurzu k datu, které připadá na státní svátek. Například pokud vyberte toto zaškrtávací políčko a použijete jako poskytovatele směnného kurzu Evropské centrální banky, systém nebude aktualizovat směnný kurz ve svátek vztahující se k aktuální právnické osobě. Tato možnost nemusí být k dispozici pro některé poskytovatele. |
| **Kurz z předchozího dne** | Toto zaškrtávací políčko je k dispozici, pokud povolíte funkci **Import ECB k aktuálnímu nebo předchozímu datu** na stránce **Správa funkcí**. Toto zaškrtávací políčko je k dispozici pouze pro poskytovatele *Central Bank of Europe*. Zaškrtněte toto políčko, chcete-li importovat směnný kurz měny, který zveřejňuje Evropská centrální banka předchozí pracovní den přibližně v 16:00 CET. Ve výchozím nastavení není toto políčko zaškrtnuto. Chcete-li importovat směnný kurz, který je publikován ve stejný pracovní den, zrušte zaškrtnutí tohoto políčka.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
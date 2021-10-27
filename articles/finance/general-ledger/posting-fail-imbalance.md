---
title: Selhání zaúčtování deníku z důvodu nevyváženosti
description: Toto téma vysvětluje, proč nemusí být debety a kredity v transakcích s poukázkami vyvážené, takže transakce nelze zaúčtovat. Téma také obsahuje kroky k vyřešení problému.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fc413f8230849653aef8c2951f1749823edded6e
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605422"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Selhání zaúčtování deníku z důvodu nevyváženosti

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, proč nemusí být debety a kredity v transakcích s poukázkami vyvážené, takže transakce nelze zaúčtovat. Téma také obsahuje kroky k vyřešení problému.

## <a name="symptom"></a>Příznak

V některých případech nelze zaúčtovat deník a zobrazí se následující zpráva: „Transakce na konkrétním dokladu nejsou k určitému datu vyrovnané (účetní měna: 0.01 - měna vykazování: 0.06).“ Proč nelze deník zaúčtovat?

## <a name="resolution"></a>Řešení

Při účtování do hlavní knihy musí být každý poukaz vyvážen v měně transakce, účetní měně a měně vykazování, pokud jsou tyto měny definovány na stránce **Nastavení hlavní knihy**. (Doklady jsou vyrovnané, když se celkové debety rovnají celkovým kreditům.)

Ve spodní části stránky řádků deníku jsou součty zobrazeny v účetní měně a měně vykazování. **Nezobrazí** se v měně transakce pro transakce v cizí měně. Chybová zpráva, kterou uživatelé obdrží během simulace nebo účtování, navíc zobrazuje rozdíly pouze v účetní měně a měně vykazování. Nezobrazuje je v měně transakce, protože jeden doklad může mít více než jednu měnu transakce a deník může obsahovat poukázky v různých měnách transakcí. Proto je důležité, abyste ručně ověřili, že částky měny transakce pro každý doklad, který má pouze jednu měnu transakce, jsou vyvážené.

### <a name="transaction-currency"></a>Měna transakce

Během simulace a účtování systém ověřuje, zda je každý doklad, který má pouze jednu měnu transakce, vyvážen v měně transakce. Pro každý zadaný doklad může existovat jedna nebo více měn pro měnu transakce. Například doklad zadaný do hlavního deníku může mít dvě měny transakcí při převodu hotovosti z bankovního účtu, který používá eura (EUR), na bankovní účet, který používá kanadské dolary (CAD).

Pokud má doklad pouze jednu měnu transakce, musí se celkové debety rovnat celkovým kreditům v měně transakce pro tento doklad. Zákazníci se setkali s následujícími scénáři, kde zaúčtování správně selhalo, protože částky měny transakce nebyly vyvážené:

- Celkový debet a celkový kredit **nebyly** vyvážené v transakční měně, ale byly vyvážené pro účetní měnu a vykazovací měnu. Zákazník předpokládal, že doklad bude přesto zaúčtován. Tento předpoklad byl však nesprávný. **Částky v měně transakce na dokladu musí být vždy vyvážené, pokud mají všechny řádky dokladu stejnou měnu transakce.**
- Doklad byl importován s datovou entitou prostřednictvím Data Management Framework (DMF) a uživatel si myslel, že částky v měně transakce jsou vyvážené. V souboru importu měly některé částky více než dvě desetinná místa a při importu částek byla zahrnuta více než dvě desetinná místa. Proto se debety nerovnaly kreditům, protože se lišily o nepatrnou částku. Deník tento rozdíl na řádcích poukázky neodrážel, protože zobrazené částky mají pouze dvě desetinná místa.
- Doklad byl importován s datovou entitou prostřednictvím DMF a uživatel si myslel, že částky měny transakce byly vyrovnané. Přestože byl **doklad** vyvážený, některé řádky na dokladu měly různá data transakcí. Pokud jste přidali celkové debety a celkové kredity v měně transakce za **doklad a datum transakce**, nebyly vyrovnané. Tento požadavek je vynucen, když zadáte doklad prostřednictvím hlavního deníku v systému. Není však vynucováno, pokud je doklad importován s datovou entitou prostřednictvím DMF.

V jednom podporovaném scénáři může mít doklad více než jednu měnu transakce. V tomto případě systém **neověřuje**, zda se debety shodují s kredity v měně transakce, protože měny se neshodují. Místo toho systém ověřuje, zda jsou částky účetní měny a měny vykazování vyvážené.

### <a name="accounting-currency"></a>Zúčtovací měna

Pokud mají všechny řádky poukázky stejnou měnu transakce a jsou-li částky měny transakce vyvážené, systém ověří, zda jsou částky účetní měny vyrovnané. Pokud je doklad zadán v cizí měně, použije se k převodu částek měny transakce na účetní měnu směnný kurz na řádcích dokladu. Každý řádek dokladu je nejprve přeložen a zaokrouhlen na dvě desetinná místa. Poté se sečtou řádky, aby se určily celkové debety a celkové kredity. Protože je přeložen každý řádek, nemusí být celkový debet a celkový kredit vyvážený. Pokud je však absolutní hodnota rozdílu v rámci hodnoty **Maximální haléřový rozdíl**, která je definována na stránce **Parametry hlavní knihy**, doklad bude zaúčtován a rozdíl bude automaticky zaúčtován na rozdílový účet.

Pokud má doklad více než jednu měnu transakce, je každý řádek dokladu přeložen do účetní měny a zaokrouhlen na dvě desetinná místa a poté jsou řádky sečteny, aby se určily celkové debety a celkové kredity. Aby byly debety a kredity považovány za vyrovnané, musí být vyrovnané, buď v přepočtu, nebo když je zahrnut rozdíl v zaokrouhlování účetní měny.

### <a name="reporting-currency"></a>Měna pro vykazování

Pokud mají všechny řádky poukázky stejnou měnu transakce a jsou-li částky měny transakce vyvážené, systém ověří, zda jsou částky měny vykazování vyrovnané. Pokud je doklad zadán v cizí měně, použije se k převodu částek měny transakce na měnu vykazování směnný kurz na řádcích dokladu. Každý řádek dokladu je nejprve přeložen a zaokrouhlen na dvě desetinná místa. Poté se sečtou řádky, aby se určily celkové debety a celkové kredity. Protože je přeložen každý řádek, nemusí být celkový debet a celkový kredit vyvážený. Pokud je však rozdíl v rámci hodnoty **Maximální haléřové zaokrouhlení v měně vykazování**, která je definována na stránce **Parametry hlavní knihy**, doklad bude zaúčtován a rozdíl bude automaticky zaúčtován na rozdílový účet.

Pokud má doklad více než jednu měnu transakce, je každý řádek dokladu přeložen do měny vykazování a zaokrouhlen na dvě desetinná místa a poté jsou řádky sečteny, aby se určily celkové debety a celkové kredity. Aby byly debety a kredity považovány za vyrovnané, musí být vyrovnané, buď v přepočtu, nebo když je zahrnut rozdíl v zaokrouhlování měny vykazování.

### <a name="example-for-an-accounting-currency-imbalance"></a>Příklad nerovnováhy účetní měny

> [!NOTE]
> Částka měny vykazování se vypočítá z částky měny transakce stejným způsobem jako částka účetní měny.

Směnný kurz: 1,5

| Řádek | Doklad | Účet | Měna | Debet (transakce) | Transakce (transakce) | Debet (účetní) | Kredit (účetní) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3.33 | | 5,00 (4,995) | |
| 2 | 001 | 1101-02 | EUR | 3.33 | | 5,00 (4,995) | |
| 3 | 001 | 1101-03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10.00 | | 15.00 |
| **Celkem** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

Účetní měna je nevyrovnaná o 0,01. Dokud je však maximální haléřové zaokrouhlení v účetní měně alespoň 0,01, rozdíl bude automaticky zaúčtován na haléřový rozdílový účet a doklad bude úspěšně zaúčtován.

---
title: Mezní limit a mezní limit výjimky
description: Tento článek popisuje mezí hodnoty a mezní hodnoty výjimek pro daň odečtenou u zdroje (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: aceebad08b5454b64059e7ef374b9634bad35c37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877929"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Mezní limit a mezní limit výjimky

[!include [banner](../includes/banner.md)]

Tento článek popisuje mezí hodnoty a mezní hodnoty výjimek pro daň odečtenou u zdroje (TDS). TDS na fakturách a platbách se vždy počítá s ohledem na mezní hodnotu a mezní hodnotu výjimky definované pro složky daně TDS na stránce **Složky srážkové daně**. Složky daně TDS jsou připojeny k daňovým kódům TDS, které jsou zahrnuty do daňových skupin TDS. Daňové skupiny TDS jsou připojeny k dodavatelům a zákazníkům k výpočtu TDS na úrovni faktury nebo platby.

TDS se vypočítá, pokud částka za transakci nebo kumulativní transakce zaúčtované u konkrétní skupiny TDS u dodavatele překročí prahovou hodnotu uvedenou na stránce **Složky srážkové daně**. TDS se nepočítá, dokud kumulativní částka transakce nepřekročí stanovený limit.

Pokud je zadána mezní hodnota výjimky spolu s mezní hodnotou složky TDS, TDS se vypočítá, když částka konkrétní transakce překročí mezní hodnotu výjimky, i když kumulativní částka transakce nepřekročí stanovenou mezní hodnotu.

### <a name="example"></a>Příklad
Daňová složka s názvem TDS je nastavena a připojena k daňové skupině TDS s názvem Dodavatel. Mezní hodnota byla definována jako 50 000 a mezní hodnota výjimky byla definována jako 20 000 pro daňovou složku TDS. Dodavatel skupiny TDS je definován jako výchozí skupina TDS pro dodavatele 1.

Nákupní faktura 001 je zaúčtována pro dodavatele 1 za 10 000. TDS se pro fakturu nevypočítává, protože částka faktury nepřekročila mezní hodnotu ani mezní hodnotu výjimky. Nákupní faktura 002 je zaúčtována pro dodavatele 1 za 25 000. TDS se pro fakturu vypočítává, protože částka faktury překročila mezní hodnotu výjimky. Nákupní faktura 003 je zaúčtována pro dodavatele 1 za 20 000. TDS se počítá pro fakturu, protože celková částka tří faktur, které jsou vystaveny pro dodavatele, překročila mezní hodnotu. TDS se počítá ze všech faktur, které jsou vystaveny pro dodavatele, u kterého nebyl TDS vypočítán dříve. Proto se TDS počítá na 30 000, což je celková částka faktury 001 a 003.

Mezní hodnota a mezní hodnota výjimky se nezohledňují při výpočtu TDS, pokud je zaškrtnuté políčko **Přehlédnout prahovou hodnotu** pro daňové kódy TDS ve skupině TDS, která je připojena k transakci. Mezní hodnota nebude použita v daňových kódech TDS ve skupině TDS, pro kterou je zaškrtávací políčko **Přehlédnout mezní hodnotu**.

Pokud je zaškrtávací políčko **Přehlédnou mezní hodnotu** zaškrtnuto pro konkrétní skupinu TDS pro některé faktury, ale není zaškrtnuto pro jiné faktury, které byly vytvořeny pro konkrétního dodavatele/zákazníka, může výpočet TDS bez překročení mezní hodnoty pro několik faktur proběhnout s ohledem na kumulativní částku u všech faktur, na které nebyl TDS dříve vypočítán.

Například mezní hodnota je 25 000. Pro dodavatele A jsou vytvořeny následující faktury.

- Faktura 1 - 20 000 - (políčko **Přehlédnout mezní hodnotu** není zaškrtnuto): TDS se nepočítá.

- Faktura 2 - 4000 - (políčko **Přehlédnout mezní hodnotu** není zaškrtnuto): TDS se počítá na 4000.

- Faktura 2 – 3000 – (políčko **Přehlédnout mezní hodnotu** není zaškrtnuto): TDS se počítá, protože kumulativní částka faktury, tj. 27 000 (20000 + 4000 + 3000), překročila mezní hodnotu. TDS se počítá z kumulativní částky faktur, u nichž nebyl TDS vypočítán dříve, tj. 23 000 (20 000 + 3000).

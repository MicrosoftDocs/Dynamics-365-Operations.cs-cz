---
title: Nastavení leasingových knih
description: Toto téma popisuje informace udržované v leasingových knihách. Leasingové knihy obsahují účetní zásady, které určují, jak je v systému účtován leasing.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441355"
---
# <a name="set-up-lease-books"></a>Nastavení leasingových knih

[!include [banner](../includes/banner.md)]

Leasingové knihy obsahují účetní zásady, které určují, jak je v systému účtován leasing. Kromě hotovostního účetnictví podporuje majetkový leasing následující standardy:

- Obecně uznávané účetní zásady ve Spojených státech (US GAAP)
- Téma kodifikace účetních standardů 842 (ASC 842)
- ASC 840
- Mezinárodní standard účetního výkaznictví 16 (IFRS 16)
- Mezinárodní účetní standard 17 (IAS 17)

Při vytváření leasingové knihy postupujte takto.

1. Přejděte na **Leasing majetku \> Nastavení \> Leasingové knihy**.
2. Vyberte **Nový** pro přidání knihy.
3. Nastavte následující pole.

    | Jméno                                     | popis |
    |------------------------------------------|-------------|
    | Účtovací vrstva                            | Vyberte účtovací vrstvu, kterou chcete použít. Každá kniha, která je připojena k leasingu, je nastavena pro konkrétní účtovací vrstvu. Každá účtovací vrstva má jiné účely zaúčtování. |
    | Typ leasingu                               | Vyberte, zda má být leasing klasifikován automaticky nebo zda má být předdefinován jako finanční nebo operativní leasing. |
    | Rámec účetnictví                     | Vyberte rámec, který je spojen s knihou. |
    | Nastavení doby trvání leasingu / očekávané doby použitelnosti          | Systém klasifikuje leasing jako finanční, pokud je typ leasingu nastaven na **automatický** a je-li doba trvání leasingu na očekávanou dobu použitelnosti majetku větší než nebo rovna procentu zadanému v tomto poli.  |
    | Nastavení současné hodnoty / reálné hodnoty majetku   | Zadejte celé číslo a definujte prahovou hodnotu, která určí typ leasingu. Pokud je současná hodnota budoucích minimálních leasingových plateb větší než uživatelem definovaná hodnota z nastavení knihy a pokud je klasifikace knihy leasingu nastavena na automatickou, systém klasifikuje leasing jako finanční leasing. |
    | Krátkodobá prahová hodnota                     | Zadejte počet měsíců, které se mají použít jako prahová hodnota pro krátkodobé leasingy. Pokud je doba leasingu menší nebo rovna počtu měsíců, které zde zadáte, systém klasifikuje leasing jako krátkodobý a použije se odložená splátka. |
    | Prahová hodnota nízké hodnoty                      | Zadejte částku, která se použije jako prahová hodnota pro leasingy aktiv s nízkou hodnotou. Pokud je reální hodnota majetku menší nebo rovna hodnotě, kterou zde zadáte, systém klasifikuje leasing jako leasing aktiv s nízkou hodnotou a použije se odložená splátka. |
    | Platba dodavateli                            | Tuto možnost nastavte na **Ano**, pokud chcete umožnit účtování leasingových plateb jako fakturu na účet dodavatele, který je uveden u každého leasingu. Po zaúčtování leasingové splátky bude připsána částka na účet dodavatele. Pokud je tato možnost nastavena na **Ne**, bude místo toho hodnota připsána na účet, který je určen pro typ zaúčtování **Leasingová platba** na stránce **Parametry zaúčtování leasingu**. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Nastavení leasingových knih
description: Tento článek popisuje informace udržované v leasingových knihách. Leasingové knihy obsahují účetní zásady, které určují, jak je v systému účtován leasing.
author: moaamer
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ee8cb3c827d590a5eb91121fe4510fbc56c13d9a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903211"
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
    | Leasingová smlouva                       | Vyberte konvenci pro datum zahájení leasingu:<ul><li><b>Žádný</b> - Jako datum zahájení se použije datum zahájení leasingu.</li><li><b>Celý měsíc</b> - Jako datum zahájení se použije první den měsíce, do kterého spadá datum zahájení leasingu.</li></ul><p>Pokud vyberete <b>Žádný</b>, existuje riziko, že plány amortizace závazků a odpisů aktiv se časově rozliší a zaúčtují náklady v polovině měsíce, nikoli na konci měsíce. Výběrem <b>Celý měsíc</b> zajistíte, že systém začne účtovat o leasingu v první den měsíce a že výdaje za celý měsíc budou připisovány a zaúčtovány v posledním dni měsíce.</p><p><strong>Poznámka:</strong> Funkce pro konvence týkající se leasingu musí být zapnutá prostřednictvím správy funkcí. V pracovním prostoru <b>Správa funkcí</b> vyhledejte a vyberte funkci, která se jmenuje <b>Konvence leasingu pro leasing majetku</b> a poté vyberte <b>Povolit nyní</b>.</p> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Datum registru DPH dodavatele
description: Tento článek poskytuje informace o funkci pro povolení data registrace dodavatele DPH
author: AdamTrukawka
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: global
ms.author: atrukawk
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.custom: intro-internal
ms.openlocfilehash: 4af770427f5b19eaf2a129b26d54aeacc6c2f148
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278271"
---
# <a name="date-of-vendor-vat-register"></a>Datum registru DPH dodavatele

V Microsoft Dynamics 365 Finance verze 10.0.24 je k dispozici pro faktury dodavatele nové pole **Datum registrace dodavatele k DPH**. Toto pole specifikuje datum uskutečnění zdanitelného plnění pro nákup.

Chcete-li povolit nové pole, přejděte na pracovní prostor **Správa funkcí** vyhledejte a vyberte funkci **Povolit datum registrace dodavatele DPH na fakturách dodavatele** a poté vyberte **Povolit nyní**.

Došlé faktury od vašich dodavatelů mohou mít dvě data: datum, kdy prodejce vystavil fakturu, a datum zdanitelného plnění (tj. datum, kdy prodejce účtoval splatnou daň z přidané hodnoty [DPH]). V některých scénářích se mohou tato dvě data lišit.

Můžete odečíst příchozí částku DPH na nákupní faktuře a zahrnout tuto fakturu do výkazů DPH později, k datu, které se liší od obou výše uvedených dat. Toto datum je u některých scénářů řízeno pravidly místní legislativy o odloženém odpočtu příchozí DPH. Liší se podle země nebo oblasti.

Některé výkazy DPH, jako např. [Kontrolní hlášení DPH](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) v Česku požadují na nákupním dokladu nahlášení data uskutečnění zdanitelného plnění. Toto datum musí být oznámeno, aby finanční úřady mohly sladit hlášení DPH mezi protistranami.

Ve Finance můžete definovat data v následujících polích:

- **Datum faktury** – Datum vystavení faktury dodavatelem.
- **Datum registrace k DPH** – Datum odpočtu částky DPH na nákupní faktuře.
- **Datum registrace dodavatele k DPH** – Datum zdanitelného plnění prodávajícího.
- **Datum přijetí dokumentu** – Datum, kdy jste obdrželi fakturu.

Tato pole jsou zahrnuta na následujících stránkách:

- Faktury dodavatele
- Registr faktur dodavatelů
- Schválení faktury dodavatele
- Deník faktur dodavatele

Po zaúčtování faktury dodavatele si můžete prohlédnout data na stránkách **Deník faktur** a **Transakce dodavatele**.

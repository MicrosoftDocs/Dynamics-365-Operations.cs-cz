---
title: Nelze změnit datum účinnosti pro schváleného dodavatele
description: Seznam schválených dodavatelů podle entity produktu neumožňuje změnu data účinnosti
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475752"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Nelze změnit datum účinnosti pro schváleného dodavatele


## <a name="symptoms"></a>Příznaky

Produkt má schváleného dodavatele, který má například datum účinnosti 11. ledna 2018 (*01/11/2018*) a datum vypršení platnosti *Nikdy*. Pokud se pokusíte změnit datum účinnosti na 10. ledna 2018 (*01/10/2018*) nebo 12. ledna 2018 (*01/12/2018*), zobrazí se následující chyba:

> Nelze vytvořit záznam v seznamu schválených dodavatelů (PdsApproveVendorList). Hodnota „Vypršení platnosti“ musí být větší nebo rovna hodnotě „Datum platnosti“.

## <a name="resolution"></a>Řešení

Můžete prodloužit pouze období, pro které je dodavatel schválen. Platí následující pravidla:

- Chcete-li změnit datum účinnosti tak, aby bylo dřívější než kterýkoli z existujících záznamů (období) pro dodavatele položky, datum vypršení platnosti nového období musí být před všemi daty vypršení platnosti v existujících záznamech.
- Chcete-li změnit datum vypršení platnosti tak, aby bylo pozdější než kterékoli z existujících období, datum platnosti musí být po posledním datu vypršení platnosti v jakémkoli existujícím záznamu.
- Chcete-li snížit celkovou dobu, po kterou je dodavatel schválen, musíte odstranit nebo upravit existující záznamy. Případně můžete použít přepínač **zkrátit** během importu. Tento přepínač odstraní všechny existující záznamy v tabulce pro schválené dodavatele podle položek.

Pro příklad scénáře, který je popsán v popisu problému, kde má záznam datum účinnosti *01/11/2018* a datum vypršení platnosti *Nikdy*, můžete importovat nový záznam, který má datum účinnosti *01/10/2018* a datum vypršení platnosti *Nikdy*. Nelze však zkrátit období tak, aby bylo datum účinnosti aktualizováno na *01/12/2018* prostřednictvím správy dat. Tuto změnu musíte provést prostřednictvím uživatelského rozhraní.

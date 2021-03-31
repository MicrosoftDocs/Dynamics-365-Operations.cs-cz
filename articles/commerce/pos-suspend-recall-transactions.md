---
title: Pozastavení a obnovení transakce v POS
description: Toto téma vysvětluje, jak mohou uživatelé pozastavit probíhající transakce a obnovit je později nebo v jiné registrační pokladně pomocí aplikace Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb92de200690b03a55a3a173fd433478c8e3175d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231265"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a>Pozastavení a obnovení transakce v POS

[!include [banner](includes/banner.md)]


Uživatelé pokladního místa mohou pozastavit probíhající transakce a následně je obnovit v jiné pokladně. Transakce jsou často pozastaveny, aby mohly rychle uvolnit registr pro jinou úlohu bez ztráty pokroku u aktuální transakce. Zaměstnanec prodejny například začne zpracovávat transakci zákazníka na mobilním zařízení, ale musí ji dokončit na pokladně, která má zásuvku s hotovostí. V takovém případě zaměstnanec obchodu může pozastavit transakci v mobilním zařízení a pak ji vyvolat a obnovit v registrační pokladně.

## <a name="configure-suspend-and-resume-functionality"></a>Konfigurovat funkci pozastavení a obnovení

### <a name="pos-operations"></a>Operace POS

Dvě [operace POS](pos-operations.md) umožňují POS podporu scénářů pozastavení a pokračování. Tyto operace můžete přiřadit k [tlačítkům mřížky](pos-screen-layouts.md) na stránce transakce nebo na úvodní stránce.

- 503: Pozastavit transakci
- 504: Odvolat transakci

### <a name="receipt-template"></a>Šablona příjmu

POS lze konfigurovat tak, aby se po pozastavení transakce generoval vytištěný doklad. Tento doklad pak slouží k rychlé identifikaci a pozdějšímu odvolání transakce.

Pokud chcete POS povolit tisk dokladu, musíte přidat formát potvrzení **pozastavení transakce** do profilu potvrzení v prodejně. Formát dokladu můžete navrhnout tak, aby obsahoval nebo vylučoval konkrétní detaily transakce. Formát může například obsahovat čárový kód podporující skenování.

### <a name="receipt-numbering"></a>Číslování účtenek

Stejně jako u ostatních typů transakcí POS, které generují tištěný doklad, můžete definovat číselnou sekvenci pozastavených transakcí v oddílu **Číslování dokladů** profilu funkce prodejny.

### <a name="void-when-closing-shift"></a>Anulovat při uzávěrce směny

Pomocí možnosti **Anulovat při zavření směny** můžete požadovat, aby uživatelé dokončili nebo anulovali jakékoli pozastavené transakce před uzavřením směny. Během operace **Zavřít směnu** POS vyzve uživatele k zobrazení nebo zrušení všech zbývajících pozastavených transakcí.

## <a name="suspend-and-resume-a-transaction"></a>Pozastavení a obnovení transakce

### <a name="suspend-a-transaction"></a>Pozastavení transakce

Uživatelé, kteří mají dostatečná oprávnění a rozložení obrazovky zahrnující operaci **Pozastavit transakci**, mohou pozastavit transakci a později ji vyvolat v jiném registru.

Transakce lze pozastavit, pouze pokud **neobsahují** následující typy řádků:

- Aktivní řádky platby
- Řádky dárkového poukazu (buď pro vydání dárkového poukazu nebo přidání k zůstatku dárkového poukazu)

Pozastavená transakce nemá vliv na informace o prodeji nebo informace o dostupnosti zásob pro obchod.

### <a name="resume-a-suspended-transaction"></a>Obnovení pozastavené transakce

Pozastavené transakce může odvolat a obnovit každý uživatel, který má dostatečná oprávnění, a který má také rozvržení, které obsahuje operaci **odvolat transakci**.

Pokud chcete rychle a snadno vyvolat pozastavenou transakci, naskenujte čárový kód na vytištěném dokladu při zobrazení seznamu transakcí z operace **Odvolat transakci**.

### <a name="considerations-for-offline-mode"></a>Co je třeba zvážit pro režim offline

- Jakákoli transakce, která je pozastavena při POS v online režimu, nemůže být obnovena v režimu offline, protože data nejsou synchronizovaná s offline databází.
- Pokud pozastavíte transakci, když je POS v režimu offline, můžete ji odvolat v režimu offline za předpokladu, že POS nebyla převedena zpět režimu online od okamžiku pozastavení transakce. Po přepnutí POS zpět do režimu online se údaje o pozastavených transakcích přesunou do online databáze a jsou odebrány z offline databáze. Transakce lze tedy obnovit pouze v režimu online. Pokud přesunete POS zpět do režimu online, nebude možné pokračovat v této pozastavené transakci vzhledem k tomu, že již byly odebrány z offline databáze.

### <a name="void-a-suspended-transaction"></a>Anulování pozastavené transakce

Anulované transakce můžete zrušit tak, že transakci odvoláte a pak provedete operaci **Anulování transakce** nebo vyberete transakci v seznamu **Odvolat transakci** a na panelu aplikace vyberete **Anulovat**. Případně lze nakonfigurovat obchod tak, aby vyzval uživatele k anulování pozastavené transakce při uzavření směny.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
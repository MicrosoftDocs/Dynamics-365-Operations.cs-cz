---
title: Nastavení a používání schopnosti rozšířeného přihlášení
description: Toto téma popisuje, jak nastavit a používat schopnost rozšířeného přihlášení v aplikaci pokladního místa (POS) Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d211ecfe1550f6093e1d35e7c2b37c036b50dd4a
ms.sourcegitcommit: 5aebb181004eb63210503fb566dcda5c55032bee
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2022
ms.locfileid: "8491432"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Nastavení a používání schopnosti rozšířeného přihlášení

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak nastavit a používat schopnost rozšířeného přihlášení v aplikaci pokladního místa (POS) Microsoft Dynamics 365 Commerce.

Cloud POS (CPOS) a Modern POS (MPOS) poskytují schopnost rozšířeného přihlášení, která umožňuje pracovníkům maloobchodu přihlásit se do aplikace POS naskenováním čárového kódu nebo přetažením karty na čtečce magnetických proužků (MSR).

## <a name="set-up-extended-logon"></a>Nastavení rozšířeného přihlášení

Chcete-li nastavit rozšířené přihlášení u registračních pokladen POS v maloobchodě, postupujte takto.

1. V centrále Commerce přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**. 
2. V levém navigačním podokně vyberte funkční profil, který je přidružen k maloobchodu.
3. Na pevné záložce **Funkce** v části **Další možnosti ověření přihlášení** nastavte následující možnosti na **Ano** nebo **Ne** podle potřeby:

    - **Přihlášení zaměstnance čárovým kódem** – Nastavte tuto možnost na **Ano** pokud chcete, aby se vaši pracovníci přihlásili do POS naskenováním čárového kódu. 
    - **Přihlášení zaměstnance vyžaduje heslo** – Nastavte tuto možnost na **Ano** pokud chcete, aby vaši pracovníci zadávali heslo během přihlášení do POS naskenováním čárového kódu.
    - **Přihlášení zaměstnance kartou** – Nastavte tuto možnost na **Ano** pokud chcete, aby se vaši pracovníci přihlásili do POS přetažením čipové karty.
    - **Přihlášení zaměstnance pomocí karty vyžaduje heslo** – Nastavte tuto možnost na **Ano** pokud chcete, aby vaši pracovníci zadávali heslo během přihlášení do POS přetažením čipové karty.

Čárový kód nebo karta jsou spojeny s přihlašovacími údaji, které lze přiřadit pracovníkovi. Přihlašovací údaje musejí mít alespoň šest znaků. Řetězec, který obsahuje prvních pět znaků, musí být jedinečný a je považován za *ID přihlašovacího údaje* který se používá k vyhledání pracovníka. Zbývající znaky se používají k ověření zabezpečení. Máte například dvě karty, z nichž jedna má přihlašovací údaje 12345DGYDEYTDW a druhá má přihlašovací údaje 12345EWUTBDAJH. Protože tyto dvě karty mají stejné identifikační číslo, 12345, nelze je obě úspěšně přiřadit pracovníkům.

## <a name="assign-extended-logon"></a>Přiřazení rozšířeného přihlášení

Ve výchozím nastavení pouze manažeři mohou přiřadit rozšířené přihlášení zaměstnancům. Chcete-li přiřadit rozšířené přihlášení, přejděte na **Rozšířené přihlášení** v POS. Pak vyhledejte pracovníka zadáním jeho ID operátora do vyhledávacího pole. Vyberte pracovníka a klikněte na možnost **Přiřadit**. Na další stránce protáhněte nebo naskenujte rozšířené přihlášení pro přiřazení pracovníka. Pokud je protáhnutí nebo naskenování úspěšné, tlačítko **OK** bude k dispozici. Klepněte na tlačítko **OK** pro uložení rozšířeného přihlášení pro tohoto pracovníka.

## <a name="delete-extended-logon"></a>Odstranění rozšířeného přihlášení

Pokud chcete odstranit rozšířené přihlášení přiřazené k pracovníkovi, vyhledejte pracovníka pomocí operace **Rozšířené přihlášení**. Vyberte pracovníka a klikněte na možnost **Zrušit přiřazení**. Budou odebrány všechny rozšířené přihlašovací údaje, které jsou přidruženy k danému pracovníkovi.

## <a name="use-extended-logon"></a>Používání rozšířeného přihlášení

Jakmile je rozšířené přihlášení nakonfigurováno a pracovník má přiřazen čárový kód nebo magnetický proužek, pracovníkovi stačí pouze protáhnout nebo naskenovat svoji kartu po zobrazení přihlašovací stránky POS. Je-li ke zpracování přihlášení nutné také heslo, pracovník je vyzván k zadání svého hesla.

## <a name="extend-extended-logon"></a>Rozšíření rozšířeného přihlášení

Přednastavená implementace schopnosti rozšířeného přihlašování vyžaduje, aby přihlašovací údaje měly minimální délku šesti znaků a aby prvních pět znaků (ID přihlašovacího údaje) bylo jedinečných. Toto bylo původně zamýšleno jako vzor, který si vývojáři mohli upravit tak, aby vyhovoval požadavkům konkrétní implementace. (Může být například přizpůsoben tak, aby podporoval více znaků nebo používal různá pravidla ověřování zabezpečení.) Podrobné informace o tom, jak sestavit rozšíření pro rozšířené přihlašování, naleznete v článku [o rozšíření funkce rozšířeného přihlašování pro MPOS a Cloud POS](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Službu pro přihlášení lze také rozšířit o podporu dalších zařízení pro rozšířené přihlášení, jako jsou čtečky dlaní. Další informace naleznete v [dokumentaci k rozšíření služby POS](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]

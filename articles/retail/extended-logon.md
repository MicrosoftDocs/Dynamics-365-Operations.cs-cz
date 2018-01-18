---
title: "Nastavení funkce rozšířeného přihlášení pro Cloud POS a MPOS"
description: "Toto téma zahrnuje možnosti pro nastavení rozšířeného přihlášení pro systém Cloud POS a Retail Modern POS (MPOS)."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e9ce03dfdc5dc027344186e0334b2ac2bc9341e
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Nastavení funkce rozšířeného přihlášení pro Cloud POS a MPOS

[!include[banner](includes/banner.md)]


Toto téma zahrnuje možnosti pro nastavení rozšířeného přihlášení pro systém Cloud POS a Retail Modern POS (MPOS).

<a name="setting-up-extended-logon"></a>Nastavení rozšířeného přihlášení
=========================

Nastavení masek čárových kódů najdete v části **Maloobchod** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Funkční profily**. Pevná záložka **Funkce** obsahuje následující volby, které se vztahují k rozšířenému přihlašování.

### <a name="staff-bar-code-logon"></a>Přihlášení zaměstnance čárovým kódem

Pokud je aktivní možnost **Přihlášení zaměstnance čárovým kódem**, mohou se pracovníci s přiřazeným rozšířeným přihlášením přihlásit k jejich pokladnímu místu pomocí čárového kódu.

### <a name="staff-bar-code-logon-requires-password"></a>Přihlášení zaměstnance pomocí čárového kódu vyžaduje heslo.

Pokud je povolena možnost **Přihlášení zaměstnance čárovým kódem vyžaduje heslo**, přihlášení zaměstnance čárovým kódem vybere pouze pracovníky, kterým je přiřazeno rozšířené přihlášení, která je uvedeno. Když je toto políčko zaškrtnuto, zaměstnanci musí i nadále zadávat své heslo.

### <a name="staff-card-logon"></a>Přihlášení zaměstnance kartou

Pokud je aktivní možnost **Přihlášení zaměstnance kartou**, mohou se pracovníci s přiřazeným rozšířeným přihlášením přihlásit k jejich pokladnímu místu pomocí magnetického proužku.

### <a name="staff-card-logon-requires-password"></a>Přihlášení zaměstnance pomocí karty vyžaduje heslo.

Pokud je povolena možnost **Přihlášení zaměstnance pomocí karty vyžaduje heslo.**, přihlášení zaměstnance kartou vybere pouze pracovníky, kterým je přiřazeno rozšířené přihlášení, která je uvedeno. Když je toto políčko zaškrtnuto, zaměstnanci musí i nadále zadávat své heslo.

<a name="assigning-an-extended-logon"></a>Přiřazení rozšířeného přihlášení
===========================

Ve výchozím nastavení pouze manažeři mohou přiřadit rozšířené přihlášení zaměstnancům. Chcete-li přiřadit rozšířené přihlášení, přejděte na **Rozšířené přihlášení** v POS. Pak vyhledejte pracovníka zadáním jeho ID operátora do vyhledávacího pole. Vyberte pracovníka a klikněte na možnost **Přiřadit**. Na další stránce protáhněte nebo naskenujte rozšířené přihlášení pro přiřazení pracovníka. Pokud je protáhnutí nebo naskenování úspěšné, tlačítko **OK** bude k dispozici. Klepněte na tlačítko **OK** pro uložení rozšířeného přihlášení pro tohoto pracovníka.

<a name="deleting-an-extended-logon"></a>Odstranění rozšířeného přihlášení
==========================

Pokud chcete odstranit rozšířené přihlášení přiřazené k pracovníkovi, vyhledejte pracovníka pomocí operace **Rozšířené přihlášení**. Vyberte pracovníka a klikněte na možnost **Zrušit přiřazení**. Budou odebrány všechny rozšířené přihlašovací údaje, které jsou přidruženy k danému pracovníkovi.

<a name="extending-extended-logon"></a>Rozšíření rozšířeného přihlášení
========================

Službu pro přihlášení lze rozšířit o podporu dalších zařízení pro rozšířené přihlášení, jako jsou čtečky dlaní. Další informace naleznete v dokumentaci k rozšíření služby POS.

<a name="using-extended-logon"></a>Používání rozšířeného přihlášení
====================

Jakmile je rozšířené přihlášení nakonfigurováno a pracovník má přiřazen čárový kód nebo magnetický proužek, pracovníkovi stačí pouze protáhnout nebo naskenovat svoji kartu po zobrazení přihlašovací stránky POS. Je-li ke zpracování přihlášení nutné také heslo, pracovník je vyzván k zadání svého hesla.





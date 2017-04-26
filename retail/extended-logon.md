---
title: "Nastavit funkci Rozšířené přihlášení pro Cloud POS a MPOS"
description: "Tato wiki zahrnuje možnosti pro nastavení rozšířeného přihlášení pro systém Cloud POS a Retail Modern POS (MPOS)."
author: josaw1
manager: AnnBe
ms.date: 2016-06-15 20 - 44 - 32
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 0dc80784a5c9a7de6009826284cb68f1aee83f70
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Nastavit funkci Rozšířené přihlášení pro Cloud POS a MPOS

Tato wiki zahrnuje možnosti pro nastavení rozšířeného přihlášení pro systém Cloud POS a Retail Modern POS (MPOS).

<a name="setting-up-extended-logon"></a>Nastavení rozšířeného přihlášení
=========================

Můžete najít nastavení masky čárového kódu na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**&gt;**funkční profily**. Pevná záložka **Funkce** obsahuje následující volby, které se vztahují k rozšířenému přihlašování.

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

Ve výchozím nastavení pouze manažeři mohou přiřadit rozšířené přihlášení zaměstnancům. Chcete-li přiřadit Rozšířené přihlášení, přejděte na **rozšířeného protokolu v** v Retail POS. Pak hledá pracovníka do pole hledání zadáte své ID operátora. Vyberte pracovníka a klikněte na možnost **Přiřadit**. Na další stránce protáhněte nebo naskenujte rozšířené přihlášení pro přiřazení pracovníka. Pokud je protáhnutí nebo naskenování úspěšné, tlačítko **OK **bude k dispozici. Klepněte na tlačítko **OK** pro uložení rozšířeného přihlášení pro tohoto pracovníka.

<a name="deleting-an-extended-logon"></a>Odstranění rozšířeného přihlášení
==========================

Pokud chcete odstranit rozšířené přihlášení přiřazené k pracovníkovi, vyhledejte pracovníka pomocí operace **Rozšířené přihlášení**. Vyberte pracovníka a klikněte na možnost **Zrušit přiřazení**. Budou odebrány všechny rozšířené přihlašovací údaje, které jsou přidruženy k danému pracovníkovi.

<a name="extending-extended-logon"></a>Rozšíření rozšířeného přihlášení
========================

Službu pro přihlášení lze rozšířit o podporu dalších zařízení pro rozšířené přihlášení, jako jsou čtečky dlaní. Další informace naleznete v dokumentaci k rozšíření služby POS.

<a name="using-extended-logon"></a>Používání rozšířeného přihlášení
====================

Jakmile je rozšířené přihlášení nakonfigurováno a pracovník má přiřazen čárový kód nebo magnetický proužek, pracovníkovi stačí pouze protáhnout nebo naskenovat svoji kartu po zobrazení přihlašovací stránky POS. Je-li ke zpracování přihlášení nutné také heslo, pracovník je vyzván k zadání svého hesla.



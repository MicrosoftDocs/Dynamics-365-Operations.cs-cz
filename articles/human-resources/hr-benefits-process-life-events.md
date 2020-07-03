---
title: Zpracování životních událostí
description: Během životního cyklu zaměstnance v aplikaci Microsoft Dynamics 365 Human Resources se může každý zaměstnanec setkat s různými změnami životních událostí.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 504408505168947ac725b5ee9764ecd994a64631
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429213"
---
# <a name="process-life-events"></a>Zpracování životních událostí

Během životního cyklu zaměstnance v aplikaci Microsoft Dynamics 365 Human Resources se může každý zaměstnanec setkat s různými změnami životních událostí. Například sňatek, změna zaměstnání nebo změna závislé osoby / příjemce. Chcete-li používat životní události, je nutné povolit životní události ve formuláři Parametry zaměstnaneckých výhod, nastavit typy životních událostí a nastavit možnosti životních událostí pro typy plánu.

Než bude možné zpracovat životní události, musí být v průběhu doby náboru již alespoň jednou spuštěna možnost otevřít registraci. V USA je otevření registrace obvykle jednou za rok. Mimo USA může být otevření registrace spuštěno v době nástupu do zaměstnání. Pracovník nemusí vybírat plán zaměstnaneckých výhod, aby mohl zpracovat životní události, ale musí být zahrnuty v procesu otevřené registrace. 

Zpracování životní události použijte, když máte pracovníky s životními událostmi, které se uskuteční v budoucnu. Tato událost zpracuje všechny životní události, které nebyly zpracovány (jako budoucí životní události nebo životní události, které byly přidány a nejsou specifické pro žádného jiného pracovníka – jedním z příkladů je nová zaměstnanecká výhoda). Životní události z reálného života jsou skryté.

Pokud je například dnes 1. února a na 14. února je naplánována změna právnických osob pro Jana Nováka, pak pokud spustíte zpracování životní události na 15. února, systém zpracuje všechny události do 15. února. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování životní události**.

2. V dialogovém okně **Spustit zpracování životní události** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Období registrace** | Období registrace pro zpracování životních událostí pro. |
   | **Právnická osoba** | Právnická osoba pro zpracování životních událostí. |
   | **Datum životní události** | Systém zpracuje všechny události během období registrace, ke kterému dojde do tohoto data. |
   | **Pracovní podproces** | Pracovník, pro něhož mají být zpracovány životní události. Pokud toto pole ponecháte prázdné, budou životní události zpracovány pro všechny pracovníky. |

3. Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:

   1. Zadejte informace pro proces.

   2. Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.

   3. Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.

   4. Vyberte **OK**. Proces bude spuštěn s nastavenými parametry.

4. Vyberte **OK**.

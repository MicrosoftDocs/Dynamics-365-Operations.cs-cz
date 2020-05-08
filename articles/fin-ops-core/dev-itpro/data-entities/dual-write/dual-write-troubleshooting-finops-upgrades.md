---
title: Poradce při potížích souvisejících s upgrady aplikací Finance and Operations
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s upgrady aplikací Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 53df00de82b101aa02160d865a9c3bbebcfcae15
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275457"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Poradce při potížích souvisejících s upgrady aplikací Finance and Operations

[!include [banner](../../includes/banner.md)]



Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service. Konkrétně obsahuje informace, které vám pomohou vyřešit problémy s upgrady aplikací Finance and Operations.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="database-synchronization-errors"></a>Chyby synchronizace databáze

**Požadovaná role pro opravu problému:** správce systému

Pokud se pokusíte pomocí entity **DualWriteProjectConfiguration** aktualizovat aplikaci Finance and Operations na Platform update 30, může se zobrazit chybová zpráva podobná následujícímu příkladu.

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Chcete-li opravit problém, postupujte následovně.

1. Přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations.
2. Spusťte Visual Studio jako správce a otevřete strom aplikačních objektů (AOT).
3. Vyhledejte **DualWriteProjectConfiguration**.
4. Ve stromu aplikačních objektů klepněte pravým tlačítkem myši na položku **DualWriteProjectConfiguration** a vyberte **Přidat do nového projektu**. Chcete-li li vytvořit nový projekt, který bude používat výchozí možnosti, klepněte na tlačítko **OK**.
5. V Průzkumníku řešení klikněte pravým tlačítkem na **Vlastnosti projektu** a lnastavte **Synchronizovat databázi na sestavení** na **True**.
6. Sestavte projekt a potvrďte, že je sestavení úspěšné.
7. V nabídce **Dynamics 365** vyberte možnost **Synchronizovat databázi**.
8. Chcete-li provést úplnou synchronizaci databáze, vyberte možnost **Synchronizovat**.
9. Po úspěšné synchronizaci celé databáze spusťte znovu krok synchronizace databáze v Lifecycle Services (LCS) Microsoft Dynamics a podle potřeby použijte skripty ručního upgradu, abyste mohli pokračovat v aktualizaci.

## <a name="missing-entity-fields-issue-on-maps"></a>Problém Chybějící pole entity u map

**Požadovaná role pro opravu problému:** správce systému

Na stránce **Dvojího zápisu** se může zobrazit chybová zpráva podobná následujícímu příkladu:

*Chybějící zdrojové pole \<název pole\> ve schématu.*

![Příklad chybové zprávy chybějícího zdrojového pole](media/error_missing_field.png)

Chcete-li tento problém vyřešit, zkontrolujte nejprve následující kroky a ujistěte se, že pole jsou v entitě.

1. Přihlaste se k modulu VM pro aplikaci Finance and Operations.
2. Přejděte na **Pracovní prostory \> Správa dat**, vyberte dlaždici **Parametry architektury** a pak na kartě **Nastavení entity** vyberte **Aktualizovat seznam entit** pro aktualizaci entit.
3. Přejděte na **Pracovní prostory \> Správa dat**, vyberte kartu **Datové entity** a zkontrolujte, zda je daná entita uvedena v seznamu. Není-li entita v seznamu uvedena, přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations a ujistěte se, že je daná entita dostupná.
4. Otevřete stránku **Mapování entit** ze stránky **Dvojí zapisování** v aplikaci Finance and Operations.
5. Chcete-li vyplnit pole v mapování entit, vyberte možnost **Aktualizovat seznam entit** .

Pokud problém stále není opraven, postupujte podle následujících kroků.

> [!IMPORTANT]
> Tento postup vás provede procesem odstranění entity a jejím opětovným přidáním. Chcete-li předejít problémům, postupujte přesně podle kroků.

1. V aplikaci Finance and Operations přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Datové entity**.
2. Vyhledejte entitu, u které chybí atribut. V panelu nástrojů klikněte na možnost **Změnit mapování cíle**.
3. V podokně **Mapovat fázování na cíl** klikněte na možnost **Generovat mapování**.
4. Otevřete stránku **Mapování entit** ze stránky **Dvojí zapisování** v aplikaci Finance and Operations.
5. Není-li atribut automaticky naplněn na mapě, přidejte jej ručně kliknutím na tlačítko **Přidat atribut** a následným kliknutím na tlačítko **Uložit**. 
6. Vyberte mapování a klikněte na tlačítko **Spustit**.

---
title: Řešení problémů s upgrady ve finančních a provozních aplikacích
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s upgrady finančních a provozních aplikací.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c7c036ef44b0470c9b3f8087e7b5b1e16dde1b34
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062818"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Řešení problémů s upgrady ve finančních a provozních aplikacích

[!include [banner](../../includes/banner.md)]





Toto téma obsahuje informace o odstraňování potíží pro integrací dvojitého zápisu mezi aplikacemi Finance a Operace a Dataverse. Konkrétně obsahuje informace, které vám pomohou vyřešit problémy s upgrady finančních a provozních aplikací.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="database-synchronization-errors"></a>Chyby synchronizace databáze

**Požadovaná role pro opravu problému:** správce systému

Pokud se pokusíte pomocí tabulky **DualWriteProjectConfiguration** aktualizovat finanční a provozní aplikaci na Platform update 30, může se zobrazit chybová zpráva podobná následujícímu příkladu.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Chcete-li opravit problém, postupujte následovně.

1. Přihlaste se k virtuálnímu počítači pro finanční a provozní aplikaci.
2. Spusťte Visual Studio jako správce a otevřete strom aplikačních objektů (AOT).
3. Vyhledejte **DualWriteProjectConfiguration**.
4. Ve stromu aplikačních objektů klepněte pravým tlačítkem myši na položku **DualWriteProjectConfiguration** a vyberte **Přidat do nového projektu**. Chcete-li li vytvořit nový projekt, který bude používat výchozí možnosti, klepněte na tlačítko **OK**.
5. V Průzkumníku řešení klikněte pravým tlačítkem na **Vlastnosti projektu** a lnastavte **Synchronizovat databázi na sestavení** na **True**.
6. Sestavte projekt a potvrďte, že je sestavení úspěšné.
7. V nabídce **Dynamics 365** vyberte možnost **Synchronizovat databázi**.
8. Chcete-li provést úplnou synchronizaci databáze, vyberte možnost **Synchronizovat**.
9. Po úspěšné synchronizaci celé databáze spusťte znovu krok synchronizace databáze v Lifecycle Services (LCS) Microsoft Dynamics a podle potřeby použijte skripty ručního upgradu, abyste mohli pokračovat v aktualizaci.

## <a name="missing-table-columns-issue-on-maps"></a>Problém s chybějícími sloupci tabulky na mapách

**Požadovaná role pro opravu problému:** správce systému

Na stránce **Dvojího zápisu** se může zobrazit chybová zpráva podobná následujícímu příkladu:

*Chybějící zdrojové pole \<field name\> ve schématu.*

![Příklad chybové zprávy chybějícího zdrojového sloupce.](media/error_missing_field.png)

Chcete-li tento problém vyřešit, zkontrolujte nejprve, že v tabulce jsou sloupce.

1. Přihlaste se k virtuálnímu počítači pro finanční a provozní aplikaci.
2. Přejděte na **Pracovní prostory \> Správa dat**, vyberte dlaždici **Parametry architektury** a pak na kartě **Nastavení tabulky** vyberte **Aktualizovat seznam tabulek** pro aktualizaci tabulek.
3. Přejděte na **Pracovní prostory \> Správa dat**, vyberte kartu **Datové tabulky** a zkontrolujte, zda je daná tabulka uvedena v seznamu. Není-li tabulka v seznamu uvedena, přihlaste se k virtuálnímu počítači pro finanční a provozní aplikaci a ujistěte se, že je daná tabulka dostupná.
4. Otevřete stránku **Mapování tabulek** ze stránky **Dvojí zapisování** ve finanční a provozní aplikaci.
5. Chcete-li vyplnit sloupce v mapování tabulky, vyberte možnost **Aktualizovat seznam tabulek** .

Pokud problém stále není opraven, postupujte podle následujících kroků.

> [!IMPORTANT]
> Tento postup vás provede procesem odstranění tabulky a jejím opětovným přidáním. Chcete-li předejít problémům, postupujte přesně podle kroků.

1. Ve finanční a provozní aplikaci přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Datové tabulky**.
2. Vyhledejte tabulku, u které chybí atribut. V panelu nástrojů klikněte na možnost **Změnit mapování cíle**.
3. V podokně **Mapovat fázování na cíl** klikněte na možnost **Generovat mapování**.
4. Otevřete stránku **Mapování tabulek** ze stránky **Dvojí zapisování** ve finanční a provozní aplikaci.
5. Není-li atribut automaticky naplněn na mapě, přidejte jej ručně kliknutím na tlačítko **Přidat atribut** a následným kliknutím na tlačítko **Uložit**. 
6. Vyberte mapování a klikněte na tlačítko **Spustit**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
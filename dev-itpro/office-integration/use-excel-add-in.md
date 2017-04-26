---
title: "Použití doplňku aplikace Excel"
description: "Toto téma vysvětluje, jak otevřít entity data v aplikaci Microsoft Excel a potom zobrazit, aktualizovat a upravovat data pomocí doplňku Microsoft Dynamics Office pro aplikaci Excel. Chcete-li otevřít entity data, můžete spustit z aplikace Excel nebo Microsoft Dynamics 365 pro operace."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Použití doplňku aplikace Excel

Toto téma vysvětluje, jak otevřít entity data v aplikaci Microsoft Excel a potom zobrazit, aktualizovat a upravovat data pomocí doplňku Microsoft Dynamics Office pro aplikaci Excel. Chcete-li otevřít entity data, můžete spustit z aplikace Excel nebo Microsoft Dynamics 365 pro operace.

Otevřením dat entity v aplikaci Microsoft Excel můžete rychle a snadno zobrazit a upravit data pomocí doplňku Microsoft Dynamics Office pro aplikaci Excel. Tento doplněk vyžaduje aplikaci Microsoft Excel 2016. **Poznámka:** Pokud vašeho klienta Microsoft Azure Active Directory (Azure AD) je nakonfigurován pro použití služby Active Directory Federation Services (AD FS), ujistěte se, že nebyla použita aktualizace květen 2016, tak, aby doplněk aplikace Excel můžete správně pro přihlášení.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Při spuštění z 365 Dynamics pro operace otevření dat entity v aplikaci Excel
1.  Na stránce 365 Microsoft Dynamics pro operace klepněte na tlačítko **otevřete v aplikaci Microsoft Office**. Pokud zdroj dat kořenové (tabulka) pro stránku je stejný jako zdroj dat kořenové pro libovolné entity, výchozí **otevřít v aplikaci Excel** možnosti, které jsou generovány pro stránku. **Otevřít v aplikaci Excel** možnosti najdete na stránkách často používané jako **všechny dodavatele** a **všechny zákazníky**.
2.  Klepněte **otevřete v aplikaci Excel** možnost a otevřete sešit, který je generován. Tento sešit obsahuje informace o vazbě pro entitu, ukazatel pro vaše prostředí a ukazatel na doplněk aplikace Excel.
3.  V aplikaci Excel, klepněte na tlačítko **povolit úpravy** Chcete-li povolit doplněk aplikace Excel spustit. Doplněk aplikace Excel spuštěna v podokně na pravé straně okna aplikace Excel.
4.  Pokud používáte doplněk aplikace Excel poprvé, klepněte na tlačítko **důvěryhodnosti Add-in**.
5.  Pokud se zobrazí výzva k přihlášení, klepněte na tlačítko **přihlášení**a potom se přihlaste pomocí stejná pověření, která jste použili pro přihlášení k Dynamics 365 pro operace. Doplněk aplikace Excel pomocí předchozí přihlašovací kontext z aplikace Internet Explorer bude a automaticky vás přihlásit, pokud je to možné. Proto ověřte uživatelské jméno v pravém horním rohu aplikace doplněk aplikace Excel.

Doplněk aplikace Excel automaticky načte data entity, kterou jste vybrali. Všimněte si, že bude žádná data v sešitu, dokud doplněk aplikace Excel načte ji.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Otevřete entitu dat v aplikaci Excel při spuštění z aplikace Excel
1.  V aplikaci Excel na **vložit** karta v **doplňky** seskupit, klikněte na **obchodu** otevřít úložiště Office.
2.  V úložišti sady Office vyhledat klíčové slovo "Dynamics" a klepněte na tlačítko **přidat** vedle **Microsoft Dynamics Office Add-in** (Excel doplněk).
3.  Pokud používáte doplněk aplikace Excel poprvé, klepněte na tlačítko **důvěryhodnosti Add-in** Chcete-li povolit doplněk aplikace Excel spustit. Doplněk aplikace Excel spuštěna v podokně na pravé straně okna aplikace Excel.
4.  Klepněte na tlačítko **přidat informace o serveru** otevřete **možností** podokno.
5.  Zkopírujte adresu URL, prohlížeč z cíle Dynamics 365 instance operace, vložte jej do **adresa URL serveru** pole a odstraňte vše za název hostitele (například odstranit **/? cmp = usmf & mi = CustTableListPage**). Výsledná adresa URL by měla mít název hostitele (například **https://xxx.dynamics.com**).
6.  Klepněte na tlačítko **OK**a potom klepněte na tlačítko **Ano** k potvrzení změny. Aplikace Excel přidat restartování a načte metadata. **Návrh** tlačítko je k dispozici. Pokud je doplněk aplikace Excel **aplety načíst** tlačítko, pravděpodobně nejste přihlášeni jako uživatel správné. Další informace naleznete v tématu "je zobrazeno tlačítko aplety zatížení" v části "Poradce při potížích" části tohoto tématu.
7.  Klepněte na tlačítko **návrh**. Doplněk aplikace Excel načte entity metadata.
8.  Klepněte na tlačítko **tabulky přidat**. Zobrazí se seznam entit. Entity jsou uvedeny ve formátu "Název – popisek".
9.  Vyberte entity v seznamu, jako například **zákazníka - odběratele**a potom klepněte na tlačítko **Další**.
10. Chcete-li přidat pole z **pole k dispozici** seznamu **vybraná pole** seznam, klepněte na pole a pak klepněte na tlačítko **přidat**. Nebo poklepejte na pole.
11. Po přidání požadovaných polí, která mají **vybraná pole** seznamu, ujistěte se, že kurzor je na správné místo v listu (například buňka A1) a potom klepněte na tlačítko **v**. Klepněte na **v** ukončíte návrháře.
12. Klepněte na tlačítko **aktualizace** přebírat v množině údajů.

## <a name="view-and-update-entity-data-in-excel"></a>Zobrazit a aktualizovat data entity v aplikaci Excel
Po doplněk aplikace Excel načte entity data do sešitu, můžete data aktualizovat kdykoli klepnutím na **aktualizace** v doplňku aplikace Excel.

## <a name="edit-entity-data-in-excel"></a>Úprava dat entity v aplikaci Excel
Můžete změnit entity data vyžadují a pak publikovat zpět klepnutím na **publikovat** v doplňku aplikace Excel. Chcete-li upravit záznam, vyberte buňku v listu a potom změňte hodnotu buňky. Chcete-li přidat nový záznam, proveďte jeden z následujících kroků:

-   Klepněte na libovolné místo v listu a potom klepněte na tlačítko **nové** v doplňku aplikace Excel.
-   Klepněte na poslední řádek listu a potom stiskněte klávesu Tab, dokud se kurzor přesune z posledního sloupce řádku a je vytvořen nový řádek.
-   Klepněte na řádek bezprostředně pod list a začít zadávat data do buňky. Při přesunutí fokusu ze buňky listu se rozšíří a bude obsahovat nový řádek.

Chcete-li odstranit záznam, postupujte jedním z následujících kroků:

-   Klepněte pravým tlačítkem na řádek číslo vedle řádku listu odstranit, a klepněte na tlačítko **odstranit**.
-   Klepněte pravým tlačítkem myši do řádku listu odstranit a potom klepněte na tlačítko **odstranit**&gt;**řádky tabulky**.

## <a name="add-or-remove-columns"></a>Přidat nebo odebrat sloupce
Chcete-li upravit sloupce, které jsou automaticky přidány do listu můžete použít návrháře.

1.  Spustit Návrhář zdroj dat doplňku aplikace Excel klepnutím **možnosti** tlačítko (symbol zařízení) a poté výběrem **povolení návrhu** políčko.
2.  Klepněte na tlačítko **návrh** v doplňku aplikace Excel. Všechny zdroje dat jsou uvedeny.
3.  V části zdroj dat klepněte **úprava** tlačítko (symbol tužky).
4.  Úprava seznamu v **vybraná pole** seznam, potřebujete:
    -   Chcete-li přidat pole z **pole k dispozici** seznamu **vybraná pole** seznam, klepněte na pole a pak klepněte na tlačítko **přidat**. Nebo poklepejte na pole.
    -   Chcete-li odebrat pole z **vybraná pole** seznam, klepněte na pole a pak klepněte na tlačítko **odstranit**. Nebo poklepejte na pole.
    -   Chcete-li změnit pořadí polí, klepněte na pole v **vybraná pole** seznamu a potom klepněte na tlačítko **se** nebo **dolů**.

5.  Použít změny na zdroj dat klepnutím na **aktualizace**. Klepněte na **v** ukončíte návrháře. Pokud jste přidali pole (sloupec), klepněte na tlačítko **aktualizace** zobrazíte aktualizované sady dat.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Existuje několik problémů, které lze vyřešit pomocí některé jednoduché kroky.

-   **Je zobrazeno tlačítko aplety načíst.** Pokud je doplněk aplikace Excel **aplety načíst** tlačítko po přihlášení, pravděpodobně nejste přihlášeni jako uživatel správné. Chcete-li tento problém vyřešit, ověřte, že správné uživatelské jméno se zobrazí v pravém horním rohu aplikace doplněk aplikace Excel. Pokud se zobrazí nesprávné uživatelské jméno, klepněte na něj, odhlášení a opětovném přihlášení.
-   **Zobrazí zpráva "Zakázán".** Pokud se zobrazí zpráva "Zakázán" při doplněk aplikace Excel načítání metadat, účet, který je přihlášen do doplňku aplikace Excel nemá oprávnění k použití služby cílené, instance nebo databáze. Chcete-li tento problém vyřešit, ověřte, že správné uživatelské jméno se zobrazí v pravém horním rohu aplikace doplněk aplikace Excel. Pokud se zobrazí nesprávné uživatelské jméno, klepněte na něj, odhlášení a opětovném přihlášení.
-   **Prostřednictvím aplikace Excel se zobrazí prázdná webová stránka.** Pokud během procesu přihlášení se otevře prázdná webová stránka, vyžaduje účet služby AD FS, ale není dostatečně přihlašovacího dialogového okna Načíst nejnovější verze aplikace Excel je spuštěn doplněk. Chcete-li tento problém vyřešit, aktualizujte verzi aplikace Excel, kterou používáte. Jste-li v podniku je odložené kanálu, aktualizovat verzi aplikace Excel, můžete [nástroj pro nasazení sady Office](https://technet.microsoft.com/library/jj219422.aspx) k [přesunout z odložené kanálu pro aktuální kanál](https://technet.microsoft.com/library/mt455210.aspx).




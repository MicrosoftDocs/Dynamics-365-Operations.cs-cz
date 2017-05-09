---
title: "Použití doplňku Excel"
description: "Toto téma vysvětluje, jak otevřít data entity v aplikaci Microsoft Excel a potom zobrazit, aktualizovat a upravovat data pomocí doplňku Microsoft Dynamics Office pro aplikaci Excel. Chcete-li otevřít data entity, můžete začít z aplikace Excel nebo Microsoft Dynamics 365 for Operations."
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

# <a name="use-the-excel-add-in"></a>Použití doplňku Excel

Toto téma vysvětluje, jak otevřít data entity v aplikaci Microsoft Excel a potom zobrazit, aktualizovat a upravovat data pomocí doplňku Microsoft Dynamics Office pro aplikaci Excel. Chcete-li otevřít data entity, můžete začít z aplikace Excel nebo Microsoft Dynamics 365 for Operations.

Otevřením entity v aplikaci Microsoft Excel můžete rychle a snadno zobrazit a upravovat data pomocí doplňku Microsoft Dynamics Office pro aplikaci Excel. Tento doplněk vyžaduje aplikaci Microsoft Excel 2016. **Poznámka:** Pokud je klient Microsoft Azure Active Directory (Azure AD) nakonfigurován pro použití služby Active Directory Federation Services (AD FS), musíte ověřit, že nebyla použita aktualizace pro květen 2016, aby vás doplněk aplikace Excel mohl správně přihlásit.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Otevření dat entity v Excelu při spuštění z Dynamics 365 for Operations
1.  Nastránce v aplikaci Microsoft Dynamics 365 for Operations klikněte na **Otevřít v sadě Microsoft Office**. Pokud je kořenový zdroj dat (tabulka) pro stránku stejný jako kořenový zdroj dat kořenové pro libovolnou entitu, jsou pro stránku generovány výchozí možnosti **Otevřít v aplikaci Excel**. Možnosti **Otevřít v aplikaci Excel** možnosti najdete na často používaných stránkách jako **Všichni dodavatelé** a **Všichni zákazníci**.
2.  Klikněte na **Otevřít v aplikaci Excel** otevřete sešit, který je generován. Tento sešit obsahuje závazné informace pro entitu, ukazatel pro vaše prostředí a ukazatel na doplněk aplikace Excel.
3.  V aplikaci Excel klepněte na tlačítko **Povolit úpravy**. Tím povolíte spuštění doplňku aplikace Excel spustil. Doplněk aplikace Excel je spuštěn v podokně na pravé straně okna aplikace Excel.
4.  Pokud používáte doplněk aplikace Excel poprvé, klepněte na **Důvěřovat tomuto doplňku**.
5.  Pokud se zobrazí výzva k přihlášení, klikněte na **Přihlásit**a potom se přihlaste pomocí stejných pověření, jaká jste použili pro přihlášení k Dynamics 365 for Operations. Doplněk aplikace Excel bude používat předchozí přihlašovací kontext z aplikace Internet Explorer a automaticky vás přihlásí, pokud je to možné. Proto ověřte uživatelské jméno v pravém horním rohu doplňku aplikace Excel.

Doplněk aplikace Excel automaticky načte data entity, kterou jste vybrali. Všimněte si, že v sešitu nebudou žádná data, dokud ho doplněk aplikace Excel nenačte.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Otevření dat entity v aplikaci Excel při spuštění z aplikace Excel
1.  V aplikaci Excel na kartě **Vložit** ve skupině **doplňky** kliknutím na **Obchod** otevřete Office Store.
2.  V Office Storu vyhledejte klíčové slovo "Dynamics" a klikněte na tlačítko **Přidat** vedle položky **Doplněk Microsoft Dynamics Office** (doplněk aplikace Excel).
3.  Pokud používáte doplněk aplikace Excel poprvé, klepněte na **Důvěřovat tomuto doplňku** pro povolení spuštění doplňku aplikace Excel. Doplněk aplikace Excel je spuštěn v podokně na pravé straně okna aplikace Excel.
4.  Klepněte na tlačítko **Přidat informace o serveru** k otevření podokna **Možnosti**.
5.  Zkopírujte adresu URL prohlížeče z instance aplikace Dynamics 365 for Operations, vložte ho do pole **Adresa URL serveru** a potom odstraňte vše za názvem hostitele (odstraňte například **/?cmp=usmf&mi=CustTableListPage**). Výsledná adresa URL by měla mít název hostitele (například **https://xxx.dynamics.com**).
6.  Kliknutím na **OK** a potom na **Ano** potvrďte změnu. Doplněk aplikace Excel se restartuje a načte metadata. Tlačítko **Návrh** je teď dostupné. Pokud má doplněk aplikace Excel tlačítko **Načíst aplety**, pravděpodobně nejste přihlášeni jako správný uživatel. Další informace naleznete v tématu "Zobrazuje se tlačítko Načíst aplety" v části "Poradce při potížích" tohoto tématu.
7.  Klikněte na možnost **Návrh**. Doplněk aplikace Excel načte metadata entity.
8.  Klikněte na **Přidat tabulku**. Zobrazí se seznam entit. Entity jsou uvedeny ve formátu "Název – popisek".
9.  Vyberte entitu v seznamu, jako například **Zákazník - zákazníci**a potom klepněte na tlačítko **Další**.
10. Chcete-li přidat pole ze seznamu **Dostupná pole** do seznamu **Vybraná pole**, klikněte na pole a potom na tlačítko **Přidat**. Nebo na pole poklepejte.
11. Po přidání požadovaných polí do seznamu **vybraná pole** se ujistěte, že kurzor je na správném místě v listu (například buňka A1) a potom klepněte na tlačítko **Hotovo**. Potom kliknutím na tlačítko **Hotovo** ukončete návrháře.
12. Klepněte na tlačítko **Aktualizovat** pro načtení sady dat.

## <a name="view-and-update-entity-data-in-excel"></a>Zobrazení a aktualizace dat entity v aplikaci Excel
Poté, co doplněk aplikace Excel načte data entity do sešitu, můžete data kdykoli aktualizovat klepnutím na **Aktualizovat** v doplňku aplikace Excel.

## <a name="edit-entity-data-in-excel"></a>Úprava dat entity v aplikaci Excel
Můžete změnit data entity podle požadavku a pak je publikovat zpět klepnutím na **Publikovat** v doplňku aplikace Excel. Chcete-li upravit záznam, vyberte buňku v listu a potom změňte hodnotu buňky. Chcete-li přidat nový záznam, proveďte jeden z následujících kroků:

-   Klepněte na libovolné místo v listu a potom klepněte na tlačítko **Nový** v doplňku aplikace Excel.
-   Klepněte na poslední řádek listu a potom stiskněte klávesu Tab, dokud se kurzor ne přesune z posledního sloupce řádku a dokud není vytvořen nový řádek.
-   Klepněte na řádek bezprostředně pod listem a začněte zadávat data do buňky. Při přesunutí fokusu z této buňky se list rozšíří a bude obsahovat nový řádek.

Chcete-li odstranit záznam, proveďte jeden z následujících kroků:

-   Klepněte pravým tlačítkem na číslo řádku vedle řádku, který chcete odstranit, a klepněte na **Odstranit**.
-   Klepněte pravým tlačítkem na číslo řádku v listu, který chcete odstranit, a klepněte na **Odstranit** &gt; **Řádky tabulky**.

## <a name="add-or-remove-columns"></a>Přidat nebo odebrat sloupce
Chcete-li upravit sloupce, které jsou automaticky přidány do listu, můžete použít návrháře.

1.  Spusťte návrháře zdroje dat doplňku aplikace Excel kliknutím na tlačítko **Možnosti** (symbol ozubeného kola) a potom zaškrtněte políčko **Povolit návrh**.
2.  Klikněte na tlačítko **Návrh** v doplňku aplikace Excel. Všechny zdroje dat jsou uvedeny.
3.  Vedle zdroje dat klepněte na tlačítko **Upravit** (symbol tužky).
4.  Podle potřeby upravte seznam v seznamu **Vybraná pole**:
    -   Chcete-li přidat pole ze seznamu **Dostupná pole** do seznamu **Vybraná pole**, klikněte na pole a potom na tlačítko **Přidat**. Nebo na pole poklepejte.
    -   Pokud chcete odebrat pole ze seznamu **Vybraná pole**, klikněte do pole a potom klikněte na **Odebrat**. Nebo na pole poklepejte.
    -   Chcete-li změnit pořadí polí, klepněte na pole v seznamu **vybraná pole** a potom klepněte na tlačítko **Nahoru** nebo **dolů**.

5.  Použijte změny na zdroj dat klepnutím na **Aktualizovat**. Potom kliknutím na tlačítko **Hotovo** ukončete návrháře. Pokud jste přidali pole (sloupec), klepněte na tlačítko **Aktualizovat** pro načtení aktualizované sady dat.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Řešení potíží
Existuje několik problémů, které lze vyřešit pomocí některé jednoduchých kroků.

-   **Je zobrazeno tlačítko Načíst aplety.** Pokud má doplněk aplikace Excel po přihlášení tlačítko **Načíst aplety**, pravděpodobně nejste přihlášeni jako správný uživatel. Chcete-li tento problém vyřešit, ověřte, že se v pravém horním rohu doplňku aplikace Excel zobrazuje správné uživatelské jméno. Pokud se zobrazí nesprávné uživatelské jméno, klepněte na něj, odhlaste se a znovu přihlaste.
-   **Dostanete zprávu "Zakázáno"** Pokud se při načítání metadat doplňkem aplikace Excel zobrazí zpráva "Zakázáno", účet, který je přihlášení k doplňku aplikace Excel, nemá oprávnění používat cílené služby, instance nebo databázi. Chcete-li tento problém vyřešit, ověřte, že se v pravém horním rohu doplňku aplikace Excel zobrazuje správné uživatelské jméno. Pokud se zobrazí nesprávné uživatelské jméno, klepněte na něj, odhlaste se a znovu přihlaste.
-   **V aplikaci Excel se zobrazí prázdná webová stránka.** Pokud se v průběhu přihlašování otevře prázdná webová stránka, účet vyžaduje AD FS, ale verze Excelu, na které je doplněk spuštěný, není dost nedávná, aby načetla přihlašovací dialog. Chcete-li tento problém vyřešit, aktualizujte verzi aplikace Excel, kterou používáte. Pokud chcete aktualizovat verzi Excelu, když jste v síti s vyřazeným kanálem, použijte [Nástroj pro nasazení Officel](https://technet.microsoft.com/library/jj219422.aspx) pro [přesunutí z vyřazeného kanálu do stávajícího](https://technet.microsoft.com/library/mt455210.aspx).




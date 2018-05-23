---
title: "Použití doplňku Excel"
description: "Toto téma vysvětluje, jak otevřít data entity v aplikaci Microsoft Excel a potom zobrazit, aktualizovat a upravovat data pomocí doplňku Microsoft Dynamics Office pro aplikaci Excel."
author: ChrisGarty
manager: AnnBe
ms.date: 04/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e0e3e86820e0857b320d832c3bf3c94757667919
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="use-the-excel-add-in"></a>Použití doplňku Excel

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak otevřít data entity v aplikaci Microsoft Excel a potom zobrazit, aktualizovat a upravovat data pomocí doplňku Microsoft Dynamics Office pro aplikaci Excel. Chcete-li otevřít data entity, můžete začít z aplikace Excel nebo Microsoft Dynamics 365 for Finance and Operations.

Otevřením dat entity v aplikaci Microsoft Excel můžete rychle a snadno zobrazit a upravovat data pomocí doplňku aplikace Excel. Tento doplněk vyžaduje aplikaci Microsoft Excel 2016.

> [!NOTE]
> Pokud je klient Microsoft Azure Active Directory (Azure AD) nakonfigurován pro použití služby Active Directory Federation Services (AD FS), musíte ověřit, že byla použita aktualizace z května 2016 pro Office, aby vás doplněk aplikace Excel mohl správně přihlásit.

Další informace o používání doplňku aplikace Excel se dozvíte v krátkém videu [Vytvoření šablony aplikace Excel pro vzory záhlaví a řádků v Dynamics 365 for Finance and Operations](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-finance-and-operations"></a>Otevření dat entity v Excelu při spuštění z aplikace Finance and Operations
1. Na stránce v aplikaci Finance and Operations zvolte **Otevřít v sadě Microsoft Office**.

    Pokud je kořenový zdroj dat (tabulka) pro stránku stejný jako kořenový zdroj dat kořenové pro libovolnou entitu, jsou pro stránku generovány výchozí možnosti **Otevřít v aplikaci Excel**. Možnosti **Otevřít v aplikaci Excel** možnosti najdete na často používaných stránkách jako **Všichni dodavatelé** a **Všichni zákazníci**.
 
2. Zvolte možnost **Otevřít v aplikaci Excel** a otevřete sešit, který je generován. Tento sešit obsahuje závazné informace pro entitu, ukazatel pro vaše prostředí a ukazatel na doplněk aplikace Excel.
3. V aplikaci Excel zvolte **Povolit úpravy**. Tím povolíte spuštění doplňku aplikace Excel. Doplněk aplikace Excel je spuštěn v podokně na pravé straně okna aplikace Excel.
4. Pokud používáte doplněk aplikace Excel poprvé, zvolte možnost **Důvěřovat tomuto doplňku**.
5. Pokud se zobrazí výzva k přihlášení, zvolte **Přihlásit** a potom se přihlaste pomocí stejných pověření, jaká jste použili pro přihlášení k aplikaci Finance and Operations. Doplněk aplikace Excel bude používat předchozí přihlašovací kontext z aplikace Internet Explorer a automaticky vás přihlásí, pokud je to možné. Proto ověřte uživatelské jméno v pravém horním rohu doplňku aplikace Excel.

Doplněk aplikace Excel automaticky načte data entity, kterou jste vybrali. Všimněte si, že v sešitu nebudou žádná data, dokud ho doplněk aplikace Excel nenačte.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Otevření dat entity v aplikaci Excel při spuštění z aplikace Excel
1. V aplikaci Excel na kartě **Vložit** ve skupině **doplňky** zvolením možnosti **Obchod** otevřete Office Store.
2. V Office Storu vyhledejte klíčové slovo **Dynamics** a zvolte **Přidat** vedle položky **Doplněk Microsoft Dynamics Office** (doplněk aplikace Excel).
3. Pokud používáte doplněk aplikace Excel poprvé, zvolte **Důvěřovat tomuto doplňku** pro povolení spuštění doplňku aplikace Excel. Doplněk aplikace Excel je spuštěn v podokně na pravé straně okna aplikace Excel.
4. Zvolte **Přidat informace o serveru** k otevření podokna **Možnosti**.
5. Ve vašem prohlížeči zkopírujte adresu URL cílové instance aplikace Finance and Operations, vložte ji do pole **Adresa URL serveru** a potom odstraňte vše za názvem hostitele. Výsledná adresa URL by měla mít pouze název hostitele.

    Například pokud je adresa URL `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, odstraňte všechno s výjimkou `https://xxx.dynamics.com`.

6. Zvolte **OK** a potom zvolením **Ano** potvrďte změnu. Doplněk aplikace Excel se restartuje a načte metadata.

    Tlačítko **Návrh** je teď dostupné. Pokud má doplněk aplikace Excel tlačítko **Načíst aplety**, pravděpodobně nejste přihlášeni jako správný uživatel. Další informace naleznete v tématu "Zobrazuje se tlačítko Načíst aplety" v části e [Poradce při potížích](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting) tohoto tématu.

7. Zvolte **Návrh**. Doplněk aplikace Excel načte metadata entity.
8. Zvolte **Přidat tabulku**. Zobrazí se seznam entit. Entity jsou uvedeny ve formátu "Název – popisek".
9. Vyberte entitu v seznamu, jako například **Zákazník - zákazníci** a potom zvolte **Další**.
10. Chcete-li přidat pole ze seznamu **Dostupná pole** do seznamu **Vybraná pole**, zvolte pole a potom zvolte **Přidat**. Případně dvakrát klikněte na pole v seznamu **Dostupná pole**.
11. Po dokončení přidání polí do seznamu **Vybraná pole** se ujistěte, že kurzor je na správném místě v listu (například buňka A1), a potom zvolte **Hotovo**. Potom zvolte **Hotovo** a ukončete návrháře.
12. Zvolte **Aktualizovat** pro načtení sady dat.

## <a name="view-and-update-entity-data-in-excel"></a>Zobrazení a aktualizace dat entity v aplikaci Excel
Poté, co doplněk aplikace Excel načte data entity do sešitu, můžete data kdykoli aktualizovat volbou možnosti **Aktualizovat** v doplňku aplikace Excel.

## <a name="edit-entity-data-in-excel"></a>Úprava dat entity v aplikaci Excel
Můžete změnit data entity podle požadavku a pak je publikovat zpět volbou možnosti **Publikovat** v doplňku aplikace Excel. Chcete-li upravit záznam, vyberte buňku v listu a potom změňte hodnotu buňky. Chcete-li přidat nový záznam, proveďte jeden z následujících kroků:

- Klikněte na libovolné místo v tabulce zdrojů dat a potom zvolte **Nový** v doplňku aplikace Excel.
- Klikněte kdekoliv v posledním řádku v tabulce zdrojů dat a potom stiskněte klávesu Tab, dokud se kurzor nepřesune z posledního sloupce řádku a dokud není vytvořen nový řádek.
- Klikněte kdekoliv v řádku bezprostředně pod tabulkou zdrojů dat a začněte zadávat data do buňky. Při přesunutí fokusu z této buňky se tabulka rozšíří a bude obsahovat nový řádek.
- Pro vazby polí záznamů záhlaví zvolte jedno z polí a potom zvolte **Nový** v doplňku aplikace Excel.

Všimněte si, že nový záznam lze vytvořit pouze v případě, že všechna klíčová a povinná pole jsou vázána na list, nebo případně pokud jsou výchozí hodnoty vyplněny pomocí podmínky filtru.

Chcete-li odstranit záznam, proveďte jeden z následujících kroků:

- Klepněte pravým tlačítkem na číslo řádku vedle řádku, který chcete odstranit, a zvolte **Odstranit**.
- Klikněte pravým tlačítkem kdekoliv v řádku sešitu, který chcete odstranit, a zvolte **Odstranit** &gt; **Řádky tabulky**.

Pokud byly zdroje dat přidány jako související zdroje dat, záhlaví je publikováno před řádky. Pokud existují závislosti mezi dalšími zdroji dat, může být třeba změnit výchozí pořadí publikování. Chcete-li změnit pořadí publikování, v doplňku aplikace Excel vyberte tlačítko **Možnosti** (symbol ozubeného kola) a poté na pevné záložce **Datový konektor** vyberte **Konfigurovat pořadí publikování**.

## <a name="add-or-remove-columns"></a>Přidat nebo odebrat sloupce
Chcete-li upravit sloupce, které jsou automaticky přidány do listu, můžete použít návrháře.

> [!NOTE]
> Pokud se tlačítko **Návrh** nezobrazí pod tlačítkem **Filtr** v doplňku aplikace, je nutné povolit návrháře zdroje dat. Vyberte tlačítko **Možnosti** (symbol ozubeného kola) a poté vyberte zaškrtávací políčko **Povolit návrh**.

1. V doplňku aplikace Excel zvolte **Návrh**. Všechny zdroje dat jsou uvedeny.
2. Vedle zdroje dat zvolte **Upravit** (symbol tužky).
3. Podle potřeby upravte seznam v seznamu **Vybraná pole**:

    - Chcete-li přidat pole ze seznamu **Dostupná pole** do seznamu **Vybraná pole**, zvolte pole a potom zvolte **Přidat**. Případně dvakrát klikněte na pole v seznamu **Dostupná pole**.
    - Pokud chcete odebrat pole ze seznamu **Vybraná pole**, zvolte pole a potom zvolte **Odebrat**. Nebo na pole poklepejte.
    - Chcete-li změnit pořadí polí v seznamu **Vybraná pole**, zvolte pole a potom zvolte **Nahoru** nebo **Dolů**.

4. Abyste provedli změny zdrojů dat, zvolte **Aktualizovat**. Potom zvolte **Hotovo** a ukončete návrháře.
5. Pokud jste přidali pole (sloupec), zvolte **Aktualizovat** pro načtení aktualizované sady dat.

## <a name="copy-environment-data"></a>Kopírovat data prostředí

Data načtená do sešitu z jednoho prostředí lze zkopírovat do jiného prostředí. Nestačí však změnit jen URL adresu připojení, protože datová mezipaměť v sešitu bude nadále zacházet s daty jako s existujícími daty. Namísto toho je nutné použít funkci Kopírovat data prostředí a publikovat data do nového prostředí jako nová data.

1. Zvolte tlačítko **Možnosti** (symbol ozubeného kola) a poté na pevné záložce **Datový konektor** zvolte **Kopírovat data prostředí**. 
2. Zadejte adresu URL serveru pro nové prostředí. 
3. Zvolte **OK** a potom zvolením **Ano** potvrďte akci. Doplněk aplikace Excel se restartuje a připojí do nového prostředí. Jakákoli existující data v sešitu budou zpracována jako nová data.

    Po restartování doplňku aplikace Excel oznámí okno se zprávou, že sešit je v režimu kopie prostředí.

4. Chcete-li zkopírovat data do nového prostředí jako nová data, vyberte **Publikovat**. Chcete-li zrušit operaci kopie prostředí a zkontrolovat existující data v novém prostředí, vyberte **Aktualizovat**.

## <a name="troubleshooting"></a>Řešení potíží
Existuje několik problémů, které lze vyřešit pomocí některé jednoduchých kroků.

- **Je zobrazeno tlačítko Načíst aplety** – Pokud má doplněk aplikace Excel po přihlášení tlačítko **Načíst aplety**, pravděpodobně nejste přihlášeni jako správný uživatel. Chcete-li tento problém vyřešit, ověřte, že se v pravém horním rohu doplňku aplikace Excel zobrazuje správné uživatelské jméno. Pokud se zobrazí nesprávné uživatelské jméno, zvolte ho, odhlaste se a znovu přihlaste.
- **Dostanete zprávu "Zakázáno"** – Pokud se při načítání metadat doplňkem aplikace Excel zobrazí zpráva "Zakázáno", účet, který je přihlášení k doplňku aplikace Excel, nemá oprávnění používat cílené služby, instance nebo databázi. Chcete-li tento problém vyřešit, ověřte, že se v pravém horním rohu doplňku aplikace Excel zobrazuje správné uživatelské jméno. Pokud se zobrazí nesprávné uživatelské jméno, zvolte ho, odhlaste se a znovu přihlaste.
- **V aplikaci Excel se zobrazí prázdná webová stránka** – Pokud se v průběhu přihlašování otevře prázdná webová stránka, účet vyžaduje AD FS, ale verze Excelu, na které je doplněk spuštěný, není dost nedávná, aby načetla přihlašovací dialog. Chcete-li tento problém vyřešit, aktualizujte verzi aplikace Excel, kterou používáte. Pokud chcete aktualizovat verzi Excelu, když jste v síti s vyřazeným kanálem, použijte [Nástroj pro nasazení Officel](https://technet.microsoft.com/library/jj219422.aspx) pro [přesunutí z vyřazeného kanálu do stávajícího](https://technet.microsoft.com/library/mt455210.aspx).


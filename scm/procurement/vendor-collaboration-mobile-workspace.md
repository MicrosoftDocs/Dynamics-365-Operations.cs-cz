---
title: "Dodavatele mobilní pracovní prostor spolupráce pro Microsoft Dynamics 365 pro provoz aplikace"
description: "Mobilní prostor spolupráce dodavatele dodavatele zůstali aktuální nákupní objednávky, které jim byly odeslány ke schválení a zobrazit informace o nových a aktualizovaných nákupních objednávek a kontaktů."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Dodavatele mobilní pracovní prostor spolupráce pro Microsoft Dynamics 365 pro provoz aplikace

Mobilní prostor spolupráce dodavatele dodavatele zůstali aktuální nákupní objednávky, které jim byly odeslány ke schválení a zobrazit informace o nových a aktualizovaných nákupních objednávek a kontaktů.

<a name="prerequisites"></a>Předpoklady
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Předpoklad</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Přečtěte si informace o Microsoft Dynamics 365 pro provoz mobilní platformu</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 pro mobilní platformu operace</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 pro operace</td>
<td>Ujistěte se, že používáte prostředí, které má Microsoft Dynamics 365 pro verzi operace 1611 a Microsoft Dynamics pro operace platformy aktualizace 3 (listopad 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobilní zařízení, které má 365 Dynamics pro operace aplikace nainstalována</span></td>
<td><span style="color: #000000;">Stáhněte 365 Dynamics pro operace aplikace z úložiště vaše mobilní aplikace.</span></td>
</tr>
<tr class="even">
<td>Opravy hotfix KB 3215650</td>
<td>Nainstalujte opravu hotfix Chcete-li povolit pracovní prostory, které jsou k dispozici 365 Dynamics pro operace.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Opravy hotfix KB 3216943</span> </span></td>
<td>Nainstalujte opravu hotfix Chcete-li povolit mobilní prostor spolupráce dodavatele.</td>
</tr>
<tr class="even">
<td>Dodavatelského uživatele musí mít přístup k webové rozhraní pro spolupráci dodavatele v 365 Dynamics pro operace a nastavení spolupráce uživatele dodavatele.</td>
<td>Postupujte podle kroků popsaných v následujících tématech nastavit a pracovat s dodavateli spolupráce webové rozhraní.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Spolupráce dodavatele se používá pro práci s externími dodavateli</a></li>
<li><a href="manage-vendor-collaboration-users.md">Správa uživatelů dodavatelské spolupráce</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Nastavení a správa dodavatelské spolupráce</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Spolupráce dodavatele se používá pro práci se zákazníky v 365 Dynamics pro operace</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Přehled
Mobilní prostor spolupráce dodavatele udržuje dodavatelů informováni o nové nákupní objednávky, takže můžete zobrazit a reagovat na nákupní objednávky v Dynamics 365 pro operace webového klienta.  

**Poznámka:** mobilní pracovní prostor má být použit jako doplněk webové rozhraní pro spolupráci dodavatele, ale nenahrazuje.  

S dodavatelem mobilní pracovní prostor spolupráce můžete zobrazit dodavatele nové nákupní objednávky, které byly odeslány ke schválení. Zobrazí informace o objednávce, jako jsou produkty, množství a požadované datum dodávky. Informace o ceně je k dispozici, v závislosti na konfiguraci jednotlivých dodavatelů.  

Při přihlášení uživatele jako dodavatel uvidí, které nákupní objednávky bylo odpovězeno nebo které nákupní objednávky stále čekají na zákazníka akce. Dodavatel může navrhly, aby jiné datum dodávky, tak čeká na nákupní objednávce zákazníka akce není ještě dohodnuté se zákazníkem. Dodavatele se také zobrazí seznam nákupních objednávek, které jsou potvrzeny, ale ještě nebyly dodány.  

Reagovat na nákupní objednávku, má dodavatel použít dodavatele spolupráce webové rozhraní je k dispozici v 365 Dynamics pro operace webového klienta. Je to také dodavatele bude kde získat další informace o pořadí, například přílohy dokumentu, adresu dodání na řádku a náklady, které jsou spojeny s dodavatelem.  

Zvláštní role zabezpečení prodejce zobrazit kontaktu osob, které jsou registrovány pro účet dodavatele. S stejné role zabezpečení dodavatele můžete zobrazit stav žádosti uživatele, který byl odeslán.  

Vytváření nových kontaktů a odeslání žádostí o nový uživatel musí provést v rozhraní spolupráce dodavatele, které je k dispozici v 365 Dynamics pro operace webového klienta.  

S mobilním prostoru může váš dodavatel:

-   Zobrazit nové nákupní objednávky odeslán dodavateli.
-   Zobrazit nákupní objednávky, aby reagoval na dodavatele a čekají na zákazníka akce.
-   Zobrazit nákupní objednávky, které jsou ve stavu potvrzených a plně neobdrželi.
-   Zobrazit informace o kontaktní osobě, který je registrován pro účet dodavatele (vyžaduje další role zabezpečení).
-   Zobrazení informací a sledovat stav požadavku uživatele odeslané dodavatelem (vyžaduje další role zabezpečení).

## <a name="get-started"></a>Začínáme
Chcete-li začít pracovat v mobilním zařízení:

1.  V úložišti mobilní aplikace stáhnout a nainstalovat 365 Microsoft Dynamics pro operace app.
2.  Spuštění aplikace v zařízení.
3.  Zadejte adresu URL aplikace Dynamics 365.
4.  Zadejte přihlášení do společnosti. Například zadejte **USMF**.
5.  Při prvním přihlášení, budete vyzváni pro uživatelské jméno a heslo pro vaše 365 Microsoft Dynamics pro účet operací. 

Po přihlášení aplikace nejsou zobrazeny žádné pracovní prostory. Zobrazení pracovní plochy na mobilní aplikace, musíte nejprve publikovat požadované pracovní prostory do 365 Dynamics pro operace app. Potřebujete systém správy oprávnění k publikování pracovního prostoru.

1.  Spusťte Dynamics 365 pro operace.
2.  Přejít na **Správa systému**&gt;**nastavení**&gt;**parametry systému**.
3.  Vyberte **Správa mobilní aplikace**.
4.  Vyberte pracovní prostor **spolupráce dodavatele** publikovat na mobilní platformy.
5.  Vyberte **publikovat pracovního prostoru**.
6.  Aktualizujte zařízení zobrazit publikované pracovní prostory.
7.  Vyberte **spolupráce dodavatele** prostoru. Budete na následující stránce.

[![Dodavatel spolupráce mobilní aplikace](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontakty
**Kontakty** stránka umožňuje zobrazit všechny kontakty, které byly vytvořeny pro účet dodavatele. Zobrazí kontaktní osoby jméno, primární e-mailovou a alias uživatele, pokud je k dispozici. Také ukazuje, zda je aktivní kontaktní osoba uživatelský účet. Při výběru kontaktu zobrazit podrobnosti o kontaktu, například které právnické osoby osoba je kontakt a kontaktní informace, například telefonní číslo nebo jinou e-mailovou adresu.

## <a name="user-requests"></a>Požadavky uživatele
**Požadavky uživatele** stránka umožňuje zobrazit všechny uživatel požaduje předložit prostřednictvím webového rozhraní spolupráce dodavatele a sledovat stav. Vyberete-li požadavek uživatele, můžete zobrazit, co bylo požadováno, přidat nebo deaktivovat uživatele, změnit zabezpečení a v tématu, které role zabezpečení bylo požadováno pro uživatele.

## <a name="purchase-orders-ready-for-review"></a>Připraveno ke kontrole nákupních objednávek
**Nákupní objednávky připraveno k revizi** stránka umožňuje zobrazit všechny nákupní objednávky, které byly odeslány zákazníkem a nebyly zodpovězeny. Můžete zobrazit vybrané informace o objednávce produktů, které požádaly a kdy dodat. Informace o ceně je dostupná pouze pokud tyto hodnoty jsou nastaveny pro dodavatele.  

Se zobrazí, zda nákupní objednávky obsahuje poznámky nebo přílohy. Chcete-li otevřít přílohy, musíte použít spolupráce dodavatele ve webovém klientovi. Vyberte **řádek nákupní objednávky** Chcete-li zobrazit všechny řádky s podrobnostmi. Všimněte si, že pro každý řádek, indikátor se zobrazí, zda existují poznámky nebo přílohy, nebo pokud je adresa dodání, který je jiný než je uvedeno v hlavičce.  

Reagovat na nákupní objednávku, musíte použít webový klient spolupráci dodavatele.

## <a name="awaiting-customer-action"></a>Čeká se na akci odběratele.
**Čeká na zákazníka akce** pro vás umožňuje stránce nákupní objednávky, které vy nebo někdo z vaší společnosti, který má také přístup ke spolupráci dodavatele odpověděli. Nákupní objednávky jsou viditelné v tomto seznamu pouze v případě, že zákazník musí provést jednu z následujících akcí na nákupní objednávce.

-   Jestliže nákupní objednávka byla zamítnuta, Zákazník by buď nutné aktualizace odeslané objednávky a odeslat znovu, nebo zrušit objednávku a znovu odeslat. Nákupní objednávka je znovu odeslán, zmizí ze **čeká na zákazníka akce** stránky.
-   Pokud se změnami přijat nákupní objednávky, zákazník musel aktualizovat původní objednávky a odeslání na revizi, nebo aktualizovat podle změny a potvrďte jej okamžitě. V obou případech nákupní objednávky z zmizí **čeká na zákazníka akce** stránky.
-   Jestliže nákupní objednávka byla přijata a zobrazí se v **čeká na zákazníka akce** stránky, to není, protože nákupní objednávka nebyla potvrzena automaticky při přijetí byla provedena. Čeká na nákupní agent pro změnu pořadí na potvrzeno. Nákupní objednávka by obvykle nepovažuje za dohodu mezi zákazníkem a dodavatelem, jakmile dodavatel přijme objednávku. Přesouvání potvrzený stav nákupní objednávky bude formality.

Výběrem nákupní objednávky se zobrazí další podrobnosti o odpověď. Můžete zobrazit podrobnosti řádku a odpovědi pro každý řádek. Zobrazí stav řádku, která z následujících odpovědí dostal.

-   Akceptováno
-   Odmítnuto
-   Přijato se změnami
-   Nahrazeno/náhradní
-   Rozdělit řádek plán nebo plán

Všimněte si, že indikátor ukazuje **doručování**= Ano/Ne, které se používá k označení, že řádky nebudou doručeny. To může být, protože řádek byl odmítnut, nahrazeno nebo kde nejsou řádky původní očekávání doručit nebo řádku, které bylo rozděleno do více řádků plánu a původní řádek nelze očekávat doručení, jak je požadováno v přijaté objednávky.  

S výjimkou odeslaných poznámky a přílohy, které lze zobrazit pomocí webového rozhraní spolupráce dodavatele jsou zobrazeny všechny změny provedené v odpovědi na řádku objednávky.

## <a name="open-confirmed-orders"></a>Otevřené objednávky potvrzené
Při potvrzení nákupní objednávky podle zákazníka, což znamená nákupní objednávce se změní na stav Potvrzeno se zobrazí v otevřít potvrzení objednávky. Zůstane v seznamu, dokud je registrována jako přijatou zákazníkem.



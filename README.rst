
==============================
|Zeroincombenze| contract 10.0
==============================
|Build Status| |Codecov Status| |license gpl| |Try Me|


.. contents::


Overview / Panoramica
=====================

|en| Odoo Contracts are special types of Analytic Accounts.
This repository provides features extending Contracts.

Dependencies on Project features should not be required.
For Project related extensions please see the
[Project](https://github.com/zeroincombenze/project) repository.


|it| Contratti Odoo sono tipi speciali di conti analitici.
Questa repository fornisce le caratteristiche per i contratti.

Alcuni modulo potrebbero dipendere dalla repository
[progetti](https://github.com/zeroincombenze/project)

Avaiable Addons / Moduli disponibili
------------------------------------

+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| Name / Nome                          | Version    | OCA Ver.   | Description / Descrizione                                                        |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| agreement_account                    | 10.0.1.0.0 | |no_check| | Adds an agreement object linked to an invoice                                    |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| agreement_sale                       | 10.0.1.0.1 | |no_check| | Link an agreement to a sale order and copy to invoice                            |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| contract                             | |halt|     | |no_check| | Contracts Management - Recurring                                                 |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| contract_digitized_signature         | 10.0.1.0.0 | |no_check| | Contract Digitized Signature                                                     |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| contract_payment_auto                | 10.0.1.0.1 | |no_check| | Adds automatic payments to contracts.                                            |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| contract_payment_mode                | 10.0.1.0.1 | |no_check| | Payment mode in contracts and their invoices                                     |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| contract_recurring_analytic_distribu | |halt|     | |no_check| | Analytic plans on contracts recurring invoices                                   |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| contract_sale                        | 10.0.1.0.0 | |no_check| | Contract from Sale                                                               |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| contract_sale_generation             | 10.0.3.0.0 | |no_check| | Contracts Management - Recurring Sales                                           |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| contract_show_invoice                | 10.0.1.0.1 | |no_check| | Button in contracts to show their invoices                                       |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| contract_variable_quantity           | 10.0.1.2.0 | |no_check| | Variable quantity in contract recurrent invoicing                                |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| product_contract                     | 10.0.1.1.0 | |no_check| | Product Contract                                                                 |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+
| website_portal_contract              | 10.0.1.0.0 | |no_check| | Extends website portal with contracts.                                           |
+--------------------------------------+------------+------------+----------------------------------------------------------------------------------+


OCA comparation / Confronto con OCA
-----------------------------------


+-----------------------------------------------------------------+-------------------+----------------+--------------------------------+
| Description / Descrizione                                       | Zeroincombenze    | OCA            | Notes / Note                   |
+-----------------------------------------------------------------+-------------------+----------------+--------------------------------+
| Coverage / Copertura test                                       |  |Codecov Status| | |OCA Codecov|  |                                |
+-----------------------------------------------------------------+-------------------+----------------+--------------------------------+


Getting started / Come iniziare
===============================

|Try Me|


Prerequisites / Prerequisiti
----------------------------


* python 2.7+ (best 2.7.5+)
* postgresql 9.2+ (best 9.5)


Installation / Installazione
----------------------------

+---------------------------------+------------------------------------------+
| |en|                            | |it|                                     |
+---------------------------------+------------------------------------------+
| These instruction are just an   | Istruzioni di esempio valide solo per    |
| example to remember what        | distribuzioni Linux CentOS 7, Ubuntu 14+ |
| you have to do on Linux.        | e Debian 8+                              |
|                                 |                                          |
| Installation is built with:     | L'installazione è costruita con:         |
+---------------------------------+------------------------------------------+
| `Zeroincombenze Tools <https://github.com/zeroincombenze/tools>`__         |
+---------------------------------+------------------------------------------+
| Suggested deployment is:        | Posizione suggerita per l'installazione: |
+---------------------------------+------------------------------------------+
| /opt/odoo/10.0/contract/                                                   |
+----------------------------------------------------------------------------+

::

    cd $HOME
    git clone https://github.com/zeroincombenze/tools.git
    cd ./tools
    ./install_tools.sh -p
    export PATH=$HOME/dev:$PATH
    odoo_install_repository contract -b 10.0 -O zero
    for pkg in os0 z0lib; do
        pip install $pkg -U
    done
    sudo manage_odoo requirements -b 10.0 -vsy -o /opt/odoo/10.0


Upgrade / Aggiornamento
-----------------------

+---------------------------------+------------------------------------------+
| |en|                            | |it|                                     |
+---------------------------------+------------------------------------------+
| When you want upgrade and you   | Per aggiornare, se avete installato con  |
| installed using above           | le istruzioni di cui sopra:              |
| statements:                     |                                          |
+---------------------------------+------------------------------------------+

::

    odoo_install_repository contract -b 10.0 -O zero -U
    # Adjust following statements as per your system
    sudo systemctl restart odoo


Support / Supporto
------------------


|Zeroincombenze| This project is mainly maintained by the `SHS-AV s.r.l. <https://www.zeroincombenze.it/>`__



Get involved / Ci mettiamo in gioco
===================================

Bug reports are welcome! You can use the issue tracker to report bugs,
and/or submit pull requests on `GitHub Issues
<https://github.com/zeroincombenze/contract/issues>`_.

In case of trouble, please check there if your issue has already been reported.

Proposals for enhancement
-------------------------


|en| If you have a proposal to change on oh these modules, you may want to send an email to <cc@shs-av.com> for initial feedback.
An Enhancement Proposal may be submitted if your idea gains ground.

|it| Se hai proposte per migliorare uno dei moduli, puoi inviare una mail a <cc@shs-av.com> per un iniziale contatto.

Credits / Didascalie
====================

Copyright
---------

Odoo is a trademark of `Odoo S.A. <https://www.odoo.com/>`__ (formerly OpenERP)


----------------


|en| **zeroincombenze®** is a trademark of `SHS-AV s.r.l. <https://www.shs-av.com/>`__
which distributes and promotes ready-to-use **Odoo** on own cloud infrastructure.
`Zeroincombenze® distribution of Odoo <https://wiki.zeroincombenze.org/en/Odoo>`__
is mainly designed to cover Italian law and markeplace.

|it| **zeroincombenze®** è un marchio registrato da `SHS-AV s.r.l. <https://www.shs-av.com/>`__
che distribuisce e promuove **Odoo** pronto all'uso sulla propria infrastuttura.
La distribuzione `Zeroincombenze® <https://wiki.zeroincombenze.org/en/Odoo>`__ è progettata per le esigenze del mercato italiano.


|chat_with_us|


|


Last Update / Ultimo aggiornamento: 2019-09-05

.. |Maturity| image:: https://img.shields.io/badge/maturity-Alfa-red.png
    :target: https://odoo-community.org/page/development-status
    :alt: Alfa
.. |Build Status| image:: https://travis-ci.org/zeroincombenze/contract.svg?branch=10.0
    :target: https://travis-ci.org/zeroincombenze/contract
    :alt: github.com
.. |license gpl| image:: https://img.shields.io/badge/licence-LGPL--3-7379c3.svg
    :target: http://www.gnu.org/licenses/lgpl-3.0-standalone.html
    :alt: License: LGPL-3
.. |license opl| image:: https://img.shields.io/badge/licence-OPL-7379c3.svg
    :target: https://www.odoo.com/documentation/user/9.0/legal/licenses/licenses.html
    :alt: License: OPL
.. |Coverage Status| image:: https://coveralls.io/repos/github/zeroincombenze/contract/badge.svg?branch=10.0
    :target: https://coveralls.io/github/zeroincombenze/contract?branch=10.0
    :alt: Coverage
.. |Codecov Status| image:: https://codecov.io/gh/zeroincombenze/contract/branch/10.0/graph/badge.svg
    :target: https://codecov.io/gh/zeroincombenze/contract/branch/10.0
    :alt: Codecov
.. |Tech Doc| image:: https://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg
    :target: https://wiki.zeroincombenze.org/en/Odoo/10.0/dev
    :alt: Technical Documentation
.. |Help| image:: https://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg
    :target: https://wiki.zeroincombenze.org/it/Odoo/10.0/man
    :alt: Technical Documentation
.. |Try Me| image:: https://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg
    :target: https://erp10.zeroincombenze.it
    :alt: Try Me
.. |OCA Codecov| image:: https://codecov.io/gh/OCA/contract/branch/10.0/graph/badge.svg
    :target: https://codecov.io/gh/OCA/contract/branch/10.0
    :alt: Codecov
.. |Odoo Italia Associazione| image:: https://www.odoo-italia.org/images/Immagini/Odoo%20Italia%20-%20126x56.png
   :target: https://odoo-italia.org
   :alt: Odoo Italia Associazione
.. |Zeroincombenze| image:: https://avatars0.githubusercontent.com/u/6972555?s=460&v=4
   :target: https://www.zeroincombenze.it/
   :alt: Zeroincombenze
.. |en| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/flags/en_US.png
   :target: https://www.facebook.com/Zeroincombenze-Software-gestionale-online-249494305219415/
.. |it| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/flags/it_IT.png
   :target: https://www.facebook.com/Zeroincombenze-Software-gestionale-online-249494305219415/
.. |check| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/check.png
.. |no_check| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/no_check.png
.. |menu| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/menu.png
.. |right_do| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/right_do.png
.. |exclamation| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/exclamation.png
.. |warning| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/warning.png
.. |same| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/same.png
.. |late| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/late.png
.. |halt| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/halt.png
.. |info| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/awesome/info.png
.. |xml_schema| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/certificates/iso/icons/xml-schema.png
   :target: https://github.com/zeroincombenze/grymb/blob/master/certificates/iso/scope/xml-schema.md
.. |DesktopTelematico| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/certificates/ade/icons/DesktopTelematico.png
   :target: https://github.com/zeroincombenze/grymb/blob/master/certificates/ade/scope/Desktoptelematico.md
.. |FatturaPA| image:: https://raw.githubusercontent.com/zeroincombenze/grymb/master/certificates/ade/icons/fatturapa.png
   :target: https://github.com/zeroincombenze/grymb/blob/master/certificates/ade/scope/fatturapa.md
.. |chat_with_us| image:: https://www.shs-av.com/wp-content/chat_with_us.gif
   :target: https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b

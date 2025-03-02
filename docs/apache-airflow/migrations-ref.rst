 .. Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

 ..   http://www.apache.org/licenses/LICENSE-2.0

 .. Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.

Reference for Database Migrations
'''''''''''''''''''''''''''''''''

Here's the list of all the Database Migrations that are executed via when you run ``airflow db upgrade``:

+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| Revision ID                    | Revises ID       | Airflow Version | Description                                                                           |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``ccde3e26fe78`` (head)        | ``092435bf5d12`` |                 | Add index on state, dag_id for queued ``dagrun``                                      |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``092435bf5d12``               | ``7b2661a43ba3`` |                 | Add ``max_active_runs`` column to ``dag_model`` table                                 |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``7b2661a43ba3``               | ``142555e44c17`` |                 | Change TaskInstance and TaskReschedule tables from execution_date to run_id.          |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``142555e44c17``               | ``54bebd308c5f`` |                 | Add ``data_interval_start`` and ``data_interval_end`` to ``DagRun``                   |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``54bebd308c5f``               | ``30867afad44a`` |                 | Adds ``trigger`` table and deferrable operator columns to task instance               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``30867afad44a``               | ``e9304a3141f0`` |                 | Rename ``concurrency`` column in ``dag`` table to`` max_active_tasks``                |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``e9304a3141f0``               | ``83f031fd9f1c`` |                 | Make XCom primary key columns non-nullable                                            |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``83f031fd9f1c``               | ``97cdd93827b8`` |                 | Improve MSSQL compatibility                                                           |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``97cdd93827b8``               | ``a13f7613ad25`` | ``2.1.3``       | Add ``queued_at`` column in ``dag_run`` table                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``a13f7613ad25``               | ``e165e7455d70`` | ``2.1.0``       | Resource based permissions for default ``Flask-AppBuilder`` views                     |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``e165e7455d70``               | ``90d1635d7b86`` | ``2.1.0``       | Add description field to ``Variable`` model                                           |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``90d1635d7b86``               | ``2e42bb497a22`` | ``2.1.0``       | Increase maximum length of pool name in ``task_instance`` table to ``256`` characters |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``2e42bb497a22``               | ``8646922c8a04`` | ``2.0.2``       | Rename ``last_scheduler_run`` column in ``DAG`` table to ``last_parsed_time``         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``8646922c8a04``               | ``449b4072c2da`` | ``2.0.2``       | Change default ``pool_slots`` to ``1``                                                |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``449b4072c2da``               | ``82b7c48c147f`` | ``2.0.2``       | Increase size of ``connection.extra`` field to handle multiple RSA keys               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``82b7c48c147f``               | ``e959f08ac86c`` | ``2.0.1``       | Remove ``can_read`` permission on config resource for ``User`` and ``Viewer`` role    |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``e959f08ac86c``               | ``64a7d6477aae`` | ``2.0.0``       | Change field in ``DagCode`` to ``MEDIUMTEXT`` for MySql                               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``64a7d6477aae``               | ``61ec73d9401f`` | ``2.0.0``       | Fix description field in ``connection`` to be ``text``                                |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``61ec73d9401f``               | ``2c6edca13270`` | ``2.0.0``       | Add description field to ``connection`` table                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``2c6edca13270``               | ``849da589634d`` | ``2.0.0``       | Resource based permissions.                                                           |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``849da589634d``               | ``45ba3f1493b9`` | ``2.0.0``       | Prefix DAG permissions.                                                               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``45ba3f1493b9``               | ``364159666cbd`` | ``2.0.0``       | add-k8s-yaml-to-rendered-templates                                                    |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``364159666cbd``               | ``52d53670a240`` | ``2.0.0``       | Add ``creating_job_id`` to ``DagRun`` table                                           |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``52d53670a240``               | ``98271e7606e2`` | ``2.0.0``       | fix_mssql_exec_date_rendered_task_instance_fields_for_MSSQL                           |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``98271e7606e2``               | ``bef4f3d11e8b`` | ``2.0.0``       | Add ``scheduling_decision`` to ``DagRun`` and ``DAG``                                 |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``bef4f3d11e8b``               | ``e1a11ece99cc`` | ``2.0.0``       | Drop ``KubeResourceVersion`` and ``KubeWorkerId``                                     |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``e1a11ece99cc``               | ``b247b1e3d1ed`` | ``2.0.0``       | Add external executor ID to TI                                                        |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``b247b1e3d1ed``               | ``e38be357a868`` | ``2.0.0``       | Add queued by Job ID to TI                                                            |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``e38be357a868``               | ``8d48763f6d53`` | ``2.0.0``       | Add ``sensor_instance`` table                                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``8d48763f6d53``               | ``8f966b9c467a`` | ``2.0.0``       | Add unique constraint to ``conn_id``                                                  |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``8f966b9c467a``               | ``3c20cacc0044`` | ``2.0.0``       | Set ``conn_type`` as non-nullable                                                     |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``3c20cacc0044``               | ``b25a55525161`` | ``2.0.0``       | Add ``run_type`` column in ``dag_run`` table                                          |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``b25a55525161``               | ``bbf4a7ad0465`` | ``2.0.0``       | Increase length of pool name                                                          |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``bbf4a7ad0465``               | ``cf5dc11e79ad`` | ``2.0.0``       | Remove id column from xcom                                                            |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``cf5dc11e79ad``               | ``03afc6b6f902`` | ``2.0.0``       | Drop ``user`` and ``chart`` table                                                     |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``03afc6b6f902``               | ``92c57b58940d`` | ``1.10.13``     | Increase length of ``Flask-AppBuilder`` ``ab_view_menu.name`` column                  |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``92c57b58940d``               | ``da3f683c3a5a`` | ``1.10.13``     | Create FAB Tables                                                                     |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``da3f683c3a5a``               | ``a66efa278eea`` | ``1.10.12``     | Add ``dag_hash`` Column to ``serialized_dag`` table                                   |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``a66efa278eea``               | ``952da73b5eff`` | ``1.10.11``     | Add Precision to ``execution_date`` in ``RenderedTaskInstanceFields`` table           |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``952da73b5eff``               | ``852ae6c715af`` | ``1.10.10``     | Add ``dag_code`` table                                                                |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``852ae6c715af``               | ``a4c2fd67d16b`` | ``1.10.10``     | Add ``RenderedTaskInstanceFields`` table                                              |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``a4c2fd67d16b``               | ``7939bcff74ba`` | ``1.10.10``     | Add ``pool_slots`` field to ``task_instance``                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``7939bcff74ba``               | ``fe461863935f`` | ``1.10.8``      | Add ``DagTags`` table                                                                 |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``fe461863935f``               | ``08364691d074`` | ``1.10.7``      | Increase length for connection password                                               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``08364691d074`` (mergepoint)  | ``a56c9515abdc``,| ``1.10.7``      | Straighten out the migrations                                                         |
|                                | ``004c1210f153``,|                 |                                                                                       |
|                                | ``74effc47d867``,|                 |                                                                                       |
|                                | ``b3b105409875`` |                 |                                                                                       |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``a56c9515abdc``               | ``c8ffec048a3b`` | ``1.10.3``      | Remove ``dag_stat`` table                                                             |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``004c1210f153``               | ``939bb1e647c8`` | ``1.10.4``      | Increase queue name size limit                                                        |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``74effc47d867``               | ``6e96a59344a4`` | ``1.10.5``      | Change ``datetime`` to ``datetime2(6)`` on MSSQL tables                               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``b3b105409875``               | ``d38e04c12aa2`` | ``1.10.7``      | Add ``root_dag_id`` to ``DAG``                                                        |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``d38e04c12aa2``               | ``6e96a59344a4`` | ``1.10.7``      | Add ``serialized_dag`` table                                                          |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``6e96a59344a4`` (branchpoint) | ``939bb1e647c8`` | ``1.10.4``      | Make ``TaskInstance.pool`` not nullable                                               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``939bb1e647c8`` (branchpoint) | ``dd4ecb8fbee3`` | ``1.10.3``      | task reschedule foreign key on cascade delete                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``dd4ecb8fbee3``               | ``c8ffec048a3b`` | ``1.10.3``      | Add schedule interval to dag                                                          |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``c8ffec048a3b`` (branchpoint) | ``41f5f12752f8`` | ``1.10.3``      | Add ``description`` and ``default_view`` column to ``dag`` table                      |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``41f5f12752f8``               | ``03bc53e68815`` | ``1.10.2``      | Add superuser field                                                                   |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``03bc53e68815`` (mergepoint)  | ``0a2a5b66e19d``,| ``1.10.2``      | Merge migrations Heads                                                                |
|                                | ``bf00311e1990`` |                 |                                                                                       |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``0a2a5b66e19d``               | ``9635ae0956e7`` | ``1.10.2``      | Add ``task_reschedule`` table                                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``bf00311e1990``               | ``dd25f486b8ea`` | ``1.10.2``      | Add index to ``task_instance`` table                                                  |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``dd25f486b8ea``               | ``9635ae0956e7`` | ``1.10.2``      | Add index on ``log`` table                                                            |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``9635ae0956e7`` (branchpoint) | ``856955da8476`` | ``1.10.0``      | Create index on ``task_fail`` table                                                   |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``856955da8476``               | ``f23433877c24`` | ``1.10.0``      | Fix Sqlite foreign key                                                                |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``f23433877c24``               | ``05f30312d566`` | ``1.10.0``      | Fix MySQL not null constraint                                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``05f30312d566`` (mergepoint)  | ``0e2a74e0fc9f`` | ``1.10.0``      | Merge migrations Heads                                                                |
|                                | ``86770d1215c0`` |                 |                                                                                       |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``86770d1215c0``               | ``27c6a30d7c24`` | ``1.10.0``      | Add kubernetes scheduler uniqueness                                                   |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``27c6a30d7c24``               | ``33ae817a1ff4`` | ``1.10.0``      | Add ``executor_config`` column to ``task_instance`` table                             |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``33ae817a1ff4``               | ``d2ae31099d61`` | ``1.10.0``      | Add Kubernetes resource check-pointing                                                |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``0e2a74e0fc9f``               | ``d2ae31099d61`` | ``1.10.0``      | Add time zone awareness                                                               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``d2ae31099d61`` (branchpoint) | ``947454bf1dff`` | ``1.8.2``       | Increase text size for MySQL (not relevant for other DBs' text types)                 |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``947454bf1dff``               | ``bdaa763e6c56`` | ``1.8.2``       | Create index on ``job_id`` column in ``task_instance`` table                          |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``bdaa763e6c56``               | ``cc1e65623dc7`` | ``1.8.2``       | Make xcom value column a large binary                                                 |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``cc1e65623dc7``               | ``127d2bf2dfa7`` | ``1.8.2``       | Add ``max_tries`` column to ``task_instance``                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``127d2bf2dfa7``               | ``5e7d17757c7a`` | ``1.7.1.3``     | Add ``dag_id``/``state`` index on ``dag_run`` table                                   |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``5e7d17757c7a``               | ``8504051e801b`` | ``1.7.1.3``     | Add ``pid`` field to ``TaskInstance``                                                 |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``8504051e801b``               | ``4addfa1236f1`` | ``1.7.1.3``     | Add indices on ``xcom`` table                                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``4addfa1236f1``               | ``f2ca10b85618`` | ``1.7.1.3``     | Add fractional seconds to MySQL tables                                                |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``f2ca10b85618``               | ``64de9cddf6c9`` | ``1.7.1.3``     | Add ``dag_stats`` table                                                               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``64de9cddf6c9``               | ``211e584da130`` | ``1.7.1.3``     | Add ``task_fail`` table                                                               |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``211e584da130``               | ``2e82aab8ef20`` | ``1.7.1.3``     | Add TI state index                                                                    |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``2e82aab8ef20``               | ``1968acfc09e3`` | ``1.7.1``       | Rename user table                                                                     |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``1968acfc09e3``               | ``bba5a7cfc896`` | ``1.7.0``       | Add ``is_encrypted`` column to variable table                                         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``bba5a7cfc896``               | ``bbc73705a13e`` | ``1.7.0``       | Add a column to track the encryption state of the 'Extra' field in connection         |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``bbc73705a13e``               | ``4446e08588``   | ``1.7.0``       | Add ``notification_sent`` column to ``sla_miss`` table                                |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``4446e08588``                 | ``561833c1c74b`` | ``1.6.2``       | Add ``start_date`` and ``end_date`` in ``dag_run`` table                              |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``561833c1c74b``               | ``40e67319e3a9`` | ``1.6.2``       | Add ``password`` column to ``user`` table                                             |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``40e67319e3a9``               | ``2e541a1dcfed`` | ``1.6.0``       | Add ``conf`` column in ``dag_run`` table                                              |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``2e541a1dcfed``               | ``1b38cef5b76e`` | ``1.6.0``       | Change ``task_instance.task_duration`` type to ``FLOAT``                              |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``1b38cef5b76e``               | ``502898887f84`` | ``1.6.0``       | Add ``dag_run`` table                                                                 |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``502898887f84``               | ``52d714495f0``  | ``1.6.0``       | Adding ``extra`` column to ``Log`` table                                              |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``52d714495f0``                | ``338e90f54d61`` | ``1.5.2``       | Add indices in ``job`` table                                                          |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``338e90f54d61``               | ``13eb55f81627`` | ``1.5.0``       | Add ``operator`` and ``queued_dttm`` to ``task_instance`` table                       |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``13eb55f81627``               | ``1507a7289a2f`` | ``1.5.0``       | Maintain history for compatibility with earlier migrations                            |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``1507a7289a2f``               | ``e3a246e0dc1``  | ``1.5.0``       | Add ``is_encrypted`` column in ``connection`` table                                   |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+
| ``e3a246e0dc1``                |                  | ``1.5.0``       | Create initial schema                                                                 |
+--------------------------------+------------------+-----------------+---------------------------------------------------------------------------------------+

.. spelling::
    branchpoint
    mergepoint

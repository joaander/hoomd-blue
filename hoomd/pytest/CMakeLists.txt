# copy python modules to the build directory to make it a working python package
set(files __init__.py
          test_attr_tuner.py
          test_balance.py
          test_box.py
          test_box_resize.py
          test_communicator.py
          test_dcd.py
          test_device.py
          test_filter_updater.py
          test_trigger.py
          test_type_parameter_dict.py
          test_typeparam.py
          test_operation.py
          test_remove_drift.py
          test_syncedlist.py
          test_triggeredops.py
          test_local_snapshot.py
          test_logging.py
          test_filter.py
          dummy.py
          test_snapshot.py
          test_state.py
          test_simulation.py
          test_table.py
          test_variant.py
          test_sorter.py
    )

install(FILES ${files}
        DESTINATION ${PYTHON_SITE_INSTALL_DIR}/pytest
       )

copy_files_to_build("${files}" "hoomd_pytest" "*.py")

set(programs pytest-openmpi.sh)
install(PROGRAMS ${programs}
        DESTINATION ${PYTHON_SITE_INSTALL_DIR}/pytest
       )

copy_files_to_build("${programs}" "hoomd_pytest_programs" "*.py")

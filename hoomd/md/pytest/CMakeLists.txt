# copy python modules to the build directory to make it a working python package
set(files __init__.py
    aniso_forces_and_energies.json
    test_active.py
    test_active_rotational_diffusion.py
    test_angle.py
    test_aniso_pair.py
    test_constrain_distance.py
    test_external.py
    test_filter_md.py
    test_bond.py
    test_dihedral.py
    test_flags.py
    test_lj_equation_of_state.py
    test_potential.py
    test_pppm_coulomb.py
    test_manifolds.py
    test_methods.py
    test_reverse_perturbation_flow.py
    test_table_pressure.py
    test_thermo.py
    test_thermoHMA.py
    forces_and_energies.json
    test_nlist.py
    test_rigid.py
    test_zero_momentum.py
    test_gsd.py
    )

install(FILES ${files}
        DESTINATION ${PYTHON_SITE_INSTALL_DIR}/md/pytest
       )

copy_files_to_build("${files}" "md_pytest" "*.py")
